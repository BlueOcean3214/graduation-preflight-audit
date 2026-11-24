# Audit scope

## Included

- `runs/**` for the six directories listed in the README (results.jsonl and prompts/**; plan.json only for the three new-data runs).
- `config/config.json`.
- `samples/*.json` (8 simulated learner fixtures).
- `B0-REPEAT-MAP.md` (B0 repeat mapping, produced read-only from results).
- `docs/GRADUATION-EXPERIMENT-DESIGN.md`, `docs/GRADUATION-EXPERIMENT-CONTRACT-REPORT.md`, `docs/GRADUATION-EXPERIMENT-EXECUTION-REPORT.md`.

## Excluded

- `experiments/graduation/runs/internal-api-smoke-*` (API smoke run, not part of the 165).
- Any `feedback.db`, knowledge base, `.rag_cache`, or database file.
- `blind_private/` and any blind-rating private mapping.
- Any `.env`, credentials, API key, token, or provider configuration.
- Application source code (available in the public PR branch).

## Pre-publication checks

Before publishing this snapshot, the source files were scanned for: API-key/Bearer patterns, `password`-like strings, phone numbers, e-mail addresses, 18-digit ID numbers, and http(s)/IPv4 endpoints. Result: 0 hits across all 45 original run artifacts (prompts, results, plan, config, samples, B0 map).

All records carry `provider` / `model` names only; no endpoint, key, or credential is present.

## Limits

- This is a file snapshot, not a proof of how it was produced. `base_sha` and `data_kind` are not present in the records (see README "Known gaps").
- Extraction copied files without modification; `MANIFEST.sha256` was computed after copying.
- The author's machine clock and the run timestamps are taken as-is; no time normalization was applied.
