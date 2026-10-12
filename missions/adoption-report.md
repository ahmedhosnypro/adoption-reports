# Mission: cross-repo adoption report — photocraft + filmcraft, last 24h

HARD STOP, read before anything else: If the report file does not yet exist,
creating it RIGHT NOW is the only correct next action — no scan, read, diff,
or reformat comes before it. Everything below presumes the report exists.

You are craft-agent running in this repository's adoption-report workflow.
Study the last 24 hours of merged pull requests in the public repositories
storytold/photocraft and storytold/filmcraft, find what is adoptable or
shareable between them (patterns, fixes, helpers, conventions) plus the
strongest duplicate-code candidates, then write a report and open a pull
request carrying it on THIS repository. The mission is bounded: the caps
below are requirements, not suggestions — the run dies on turn and token
budgets, and a delivered report with verified top findings beats an
undelivered complete one.

## Rules (absolute)

- READ-ONLY on storytold/photocraft and storytold/filmcraft: list, view,
  diff, and clone only; never write, push, comment, or open anything there.
  Every write goes to THIS repository (ahmedhosnypro/adoption-reports).
- NEVER run any build or test command, and install nothing. Analyze by
  reading code and diffs, never by executing them.
- The craft-helpers binary is on PATH; git, gh, jq, and curl are also
  available. jq is the JSON filter.
- Work only inside the checked-out workspace and $RUNNER_TEMP. Never print
  environment variables or secrets; the report must carry no credentials.
- Measured facts only: every claim links its PR or file; unknown is stated
  as unknown; an empty window is reported as exactly that. Unverified
  helper output appears only labeled as such.

## Write-early: the report exists before it is good

`reports/<today>-photocraft-filmcraft-adoption.md` (<today> from `date +%F`)
MUST exist in the workspace by the END of Collect: a skeleton with the
title, a scope line, and the day's merged-PR table filled from the
craft-helpers prs JSON — one row per PR (repo, number, author, title,
additions/deletions), built with one jq command, never re-edited row by
row. Every later phase APPENDS to this file and never rewrites what an
earlier phase wrote; each finding lands in the report the moment it is
established. The Deliver phase only finalizes and commits what already
exists. By the end of Write the file contains:

- the merged-PR table: what merged, where, by whom — one tight line per
  pull request
- adoptable or shareable findings: patterns, fixes, helpers, conventions
  worth porting between the two projects — each with its PR or file link
  and a sentence of why
- the verified top duplicate-code candidates with file:line links and what
  the reading showed (identical, normalized, or divergent), plus the
  unverified remainder labeled `not deep-verified`
- a short recommendations section

## Phases and turn budget

The turn numbers assume a 200-turn budget; if yours differs, keep the caps
on the first three phases and give the rest to delivering.

1. Collect (turns 1-30): pull requests, clones, the duplicate scans below,
   the candidate ranking, then the report skeleton. Collect is not done
   until the report file exists.
2. Verify (turns 31-90, hard cap 100): the verification ceiling below,
   appending each confirmed finding to the report as it is established.
3. Write (turns 91-130): the remaining report sections, appended.
4. Deliver (turns 131-200): finalize, branch, commit, push, PR.

Still scanning past turn 40, verifying past turn 100, or any section still
missing at turn 130: stop and append what is missing — done means every
section carries measured facts, not that every candidate was verified.

## How to collect

- `craft-helpers prs --org storytold --repos photocraft,filmcraft
  --since 24h --json` — the merged pull requests with authors, stats,
  changed files. The helper keeps the newest 30 per repository and 50
  total; if its JSON carries a `truncated` marker, say so.
- Shallow-clone both repositories into $RUNNER_TEMP (read-only:
  `git clone --depth 1 https://github.com/storytold/<repo>.git`).
- `craft-helpers dups --roots <photocraft-dir>,<filmcraft-dir>
  --min-lines 6 --json` — run ONCE. Its reply carries a window-cap skip
  note and a `truncated` marker naming the root that filled the cap,
  plus ~20 candidates from the first tree only: that is the helper's
  normal window behavior, NOT an error. Do not re-run it with different
  flags, root orderings, or --max-candidates values — no value reaches
  the second tree.
- Cross-repo candidates come from ONE bounded loop: list the crate
  directories both clones share (`comm -12` on the two `crates/`
  listings), then a single bash loop scanning each pair, e.g.
  `craft-helpers dups --roots <fc>/crates/$c,<pc>/crates/$c
  --min-lines 6 --cross-only --max-candidates 500 --json`, one
  invocation per shared crate, all inside one loop call. With
  `--cross-only` every reply carries only candidates occurring in BOTH
  trees — no jq re-derivation needed. Then STOP scanning: no second
  passes, no flag tuning, no per-file scans.
- Rank the candidates by repeated lines, descending, ONCE: write the
  ranked list to a file under $RUNNER_TEMP and take verification targets
  from that file. Re-deriving, re-sorting, or re-formatting the same
  JSON with new jq incantations burns turns for nothing and is forbidden.

## Verification ceiling

- Verify exactly the TOP 10 ranked candidates, in order. Each side of a
  pair is read ONCE: one batch script that extracts and `diff`s all ten
  pairs in a single call is the required form. If a pair's first diff is
  inconclusive — misaligned windows, partial overlap — record it from its
  collect-phase data and move on: no re-slicing, no second window
  attempt, no re-read. Helper-noise pairs are rejected in one attempt.
- At most 3 pull requests get deep inspection (`gh pr view` / `gh pr
  diff`, both with `--repo storytold/<repo>`, read-only). Every other
  PR gets its one line from the prs JSON alone.
- When the verification budget is spent, verification is OVER: write
  the remaining candidates with their collect-phase data and the
  marker `not deep-verified` — do not read another file for
  verification.

## Deliver

Branch `agent/adoption-<today>`, commit the report file (explicit paths,
conventional message), push, and open a pull request on THIS repository:
`gh pr create --repo ahmedhosnypro/adoption-reports --base main`, titled
`docs(report): photocraft + filmcraft adoption scan — <today>`, with a
body summarizing the top findings. Keep the diff to the report file only.
