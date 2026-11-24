# Graduation Experiment Audit Snapshot (read-only)

This repository is a **read-only snapshot of the graduation experiment's run artifacts**, published solely so an external reviewer can audit the data against the frozen design (`docs/GRADUATION-EXPERIMENT-DESIGN.md`, §7.1) and the preflight contract (`docs/GRADUATION-EXPERIMENT-CONTRACT-REPORT.md`).

It is **not** the application source, **does not** affect `BlueOcean3214/AI-Study-Assistant`, and **must not** be treated as a new data source.

## What this data is

All learner records here are **simulated learner fixtures** (`data_kind = simulated_learner_fixture` by design, §3.4). They are not real users, real feedback, or production data. No `feedback.db`, no `blind_private/`, no API keys, and no personal data are included.

## Provenance

| Item | Value |
| --- | --- |
| Source repository | `BlueOcean3214/AI-Study-Assistant` |
| Source branch | `feat/graduation-preflight-integrity` (PR #26) |
| Source HEAD at extraction | `df155a5c145297bc5e6a085636fadfd6185586bd` |
| Experiment baseline commit (per execution report) | `e5f97e9fd9d721af24ed5d7a6c047ff305fd3fcd` |
| Source path on the author's machine | `F:\somethingProject\dsbot\experiments\graduation` |
| Extraction time | 2026-11-24 (Asia/Shanghai) |
| Files / size | 57 files / ~1.5 MB |

## Contents

```
runs/main-20261113T061051Z/             140 records (A/B/C/D x S1-S7 x 5), plan.json present
runs/suppl-subj-20261113T062711Z/       10 records (C-subj / D-subj), plan.json present
runs/suppl-s7empty-20261113T062822Z/     5 records (S7-empty, D only), plan.json present
runs/b0-remainder-20261113T013105Z/      8 records (B0 repeats 2-5 for S5/S7), results only
runs/20261112T210000-20261113T011751Z/   1 record  (B0 S5 repeat 1, smoke run), results only
runs/20261112T210000-20261113T012031Z/   1 record  (B0 S7 repeat 1, smoke run), results only
B0-REPEAT-MAP.md                         B0 repeat mapping (design-sanctioned merge table)
config/config.json                       experiment configuration (knowledge_results=[], seed, ref_date, ...)
samples/S1.json ... S8.json              8 simulated learner fixtures
docs/                                    frozen design v4.5, contract report (round 11), execution report
MANIFEST.sha256                          SHA-256 of every file in this repository
AUDIT-SCOPE.md                           exact inclusion/exclusion rules and pre-publication checks
```

For the three new-data run directories, `plan.json` fixes the schedule. The three B0 legacy directories are **results-only by design** (legacy, v4.1 and earlier): they have no `plan.json`, which is exactly why the preflight contract treats them separately. Each `results.jsonl` holds one JSON record per generation; `prompts/<sample>/<group>.txt` holds the exact rendered prompt (bound to the record by `prompt_sha256`).

## Verify integrity

`.gitattributes` disables EOL conversion, so every file is stored and checked out byte-for-byte and the manifest matches on any platform.

```powershell
Get-Content MANIFEST.sha256 | ForEach-Object {
  $hash, $path = $_ -split '  ', 2
  $actual = (Get-FileHash -Algorithm SHA256 -LiteralPath $path).Hash.ToLower()
  if ($actual -ne $hash) { Write-Host "MISMATCH $path" }
}
```

## Known gaps (do not infer these from absence)

The preflight contract records seven §7.1 fields as **required but unrecoverable** in this dataset: `run_id`, `base_sha`, `knowledge_result_ids`, `memory_injected`, `short_term_injected`, `difficult_flag`, `data_kind`. See CONTRACT-REPORT §3 and §16 for the current decision state; whether (and how) they can be derived from hash-bound prompts is the subject of the audit this repository supports.

## License / use

Internal audit use only. No license is granted for redistribution. Delete this repository once the audit is complete, if the author requests it.
