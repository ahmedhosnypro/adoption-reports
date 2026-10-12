# adoption-reports

Public sink for craft-agent adoption reports. The `adoption-report`
workflow studies the last 24 hours of merged pull requests in
[storytold/photocraft](https://github.com/storytold/photocraft) and
[storytold/filmcraft](https://github.com/storytold/filmcraft) — strictly
read-only — and delivers an evidence-cited report of adoptable patterns
and duplicate-code candidates as a pull request on this repository.

## Trigger

Actions tab → **Cross-repo adoption report** → **Run workflow**
(workflow_dispatch; no other event starts it). Runs are serialized;
one report at a time.

## What lands

- `reports/<date>-photocraft-filmcraft-adoption.md` — the report
- a branch `agent/adoption-<date>` and one pull request titled
  `docs(report): photocraft + filmcraft adoption scan — <date>`
- the run's stream-json transcript as a workflow artifact
  (`run-transcript`)

## What a run does

1. Clones the private repository of the model gateway (the token
   rides an http.extraheader — never a URL, never a log line).
2. Restores its registry dump into a local postgres:17 and boots the
   prebuilt gateway binary on 127.0.0.1:17844 — a local model
   gateway serving the OpenAI-compatible API that craft-agent calls.
3. Downloads craft-agent and craft-helpers from the private
   ahmedhosnypro/craft-agent release (tag pinned by
   `CRAFT_AGENT_VERSION` in the workflow) and sha256-verifies both.
4. Runs `craft-agent run --agent adoption-analyst --prompt
   missions/adoption-report.md` against the local gateway; the agent
   profile is `.craft-agent/agents/adoption-analyst.md`.

## Secrets (names only — Settings → Secrets and variables → Actions)

| name | used for |
| --- | --- |
| `PRIVATE_REPO_ACCESS_TOKEN` | authed clone of the private gateway repository; private release downloads |
| `IR_MASTER_KEY` | gateway provider-key decryption master key |
| `GATEWAY_DB_PASSWORD` | the runner's local postgres password |
| `MODEL_API_URL` | base URL of the gateway's OpenAI-compatible API |
| `MODEL_API_KEY` | the API key craft-agent presents to the gateway |
| `MODEL_ID` | the model id (glm-5.3-flash) |

## Goal

Today this repository consumes craft-agent by downloading its private
release binaries each run. When craft-agent publishes as an official
public action, the run step switches to
`uses: ahmedhosnypro/craft-agent@v1` and the download step is deleted.
