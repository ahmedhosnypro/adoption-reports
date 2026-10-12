# adoption-reports

Public sink for craft-agent adoption scans. The `adoption-scan` workflow
studies the last 24 hours of merged pull requests in
[storytold/photocraft](https://github.com/storytold/photocraft) and
[storytold/filmcraft](https://github.com/storytold/filmcraft) — strictly
read-only — and delivers an evidence-cited report of adoptable patterns
and duplicate-code candidates as a pull request on this repository.

## Trigger

Actions tab → **adoption-scan** → **Run workflow** (workflow_dispatch;
no other event starts it). Runs are serialized; one scan at a time.

## What lands

- `reports/<date>-photocraft-filmcraft-adoption.md` — the report
- a branch `agent/adoption-<date>` and one pull request titled
  `docs(report): photocraft + filmcraft adoption scan — <date>`
- the run's stream-json transcript as a workflow artifact

## What a run does

1. Clones the private gateway repository (the token rides an
   http.extraheader — never a URL, never a log line).
2. Restores its registry dump into a local postgres:17 and boots the
   prebuilt gateway binary on 127.0.0.1:17844.
3. Downloads craft-agent and craft-helpers from the private
   ahmedhosnypro/craft-agent release (tag pinned by
   `CRAFT_AGENT_VERSION` in the workflow) and sha256-verifies both.
4. Runs `craft-agent run --agent adoption-scan --prompt
   missions/adoption-scan.md` against the local gateway; the agent
   profile is `.craft-agent/agents/adoption-scan.md`.

## Secrets (names only — Settings → Secrets and variables → Actions)

| name | used for |
| --- | --- |
| `PRIVATE_REPO_TOKEN` | authed clone of the private gateway repo; private release downloads |
| `IR_MASTER_KEY` | gateway provider-key decryption master key |
| `IRONROUTER_DB_PASSWORD` | the runner's local postgres password |
| `IRONROUTER_CLIENT_KEY` | gateway caller key for the readiness probe |
| `BYOK_BASE_URL` | the OpenAI-compatible base URL craft-agent calls |
| `BYOK_API_KEY` | the caller key craft-agent presents |
| `BYOK_MODEL` | the model id (glm-5.3-flash) |

## Goal

Today this repository consumes craft-agent by downloading its private
release binaries each run. When craft-agent publishes as an official
public action, the run step switches to
`uses: ahmedhosnypro/craft-agent@v1` and the download step is deleted.
