# B0 重复编号映射（S5、S7 各 5 次）

- 生成方式：只读三份 `results.jsonl` 汇总，未修改任何原始结果文件，也未改动任何实验代码。
- 口径：原两份冒烟记录 = 每格第 1 次；`b0-remainder-20261113T013105Z` 的 `repeat_index=0–3` = 第 2–5 次。
- 合并统计时以本表「B0 第 n 次」为准，不要直接混用不同 run-dir 的 `repeat_index`。

| 样本 | B0 第 n 次 | sample_id | group | repeat_index（原始） | experiment_id | run-dir | provider / model | temperature / top_p / max_tokens | prompt_sha256 | success | request_count | corrections | prompt_tokens | completion_tokens | total_tokens | stopped_reason | generated_at |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| S5 | 1 | S5 | B0 | 0 | graduation-memory-ablation@20261112T210000@20261112T210000-20261113T011751Z | 20261112T210000-20261113T011751Z | openai_compatible / santuo-workbuddy | 0.7 / 1.0 / 2048 | 1676ec368b81903b649433928029a0e77e6b815600ec56155ef0cf48a96a605e | True | 1 | 0 | 971 | 1134 | 2105 | plan_draft_ready | 2026-11-13T09:17:59+08:00 |
| S5 | 2 | S5 | B0 | 0 | graduation-memory-ablation@20261112T210000@b0-remainder-20261113T013105Z | b0-remainder-20261113T013105Z | openai_compatible / santuo-workbuddy | 0.7 / 1.0 / 2048 | 1676ec368b81903b649433928029a0e77e6b815600ec56155ef0cf48a96a605e | True | 1 | 0 | 971 | 539 | 1510 | plan_draft_ready | 2026-11-13T09:31:10+08:00 |
| S5 | 3 | S5 | B0 | 1 | graduation-memory-ablation@20261112T210000@b0-remainder-20261113T013105Z | b0-remainder-20261113T013105Z | openai_compatible / santuo-workbuddy | 0.7 / 1.0 / 2048 | 1676ec368b81903b649433928029a0e77e6b815600ec56155ef0cf48a96a605e | True | 1 | 0 | 971 | 932 | 1903 | plan_draft_ready | 2026-11-13T09:31:16+08:00 |
| S5 | 4 | S5 | B0 | 2 | graduation-memory-ablation@20261112T210000@b0-remainder-20261113T013105Z | b0-remainder-20261113T013105Z | openai_compatible / santuo-workbuddy | 0.7 / 1.0 / 2048 | 1676ec368b81903b649433928029a0e77e6b815600ec56155ef0cf48a96a605e | True | 1 | 0 | 971 | 719 | 1690 | plan_draft_ready | 2026-11-13T09:31:20+08:00 |
| S5 | 5 | S5 | B0 | 3 | graduation-memory-ablation@20261112T210000@b0-remainder-20261113T013105Z | b0-remainder-20261113T013105Z | openai_compatible / santuo-workbuddy | 0.7 / 1.0 / 2048 | 1676ec368b81903b649433928029a0e77e6b815600ec56155ef0cf48a96a605e | True | 1 | 0 | 971 | 1208 | 2179 | plan_draft_ready | 2026-11-13T09:31:27+08:00 |
| S7 | 1 | S7 | B0 | 0 | graduation-memory-ablation@20261112T210000@20261112T210000-20261113T012031Z | 20261112T210000-20261113T012031Z | openai_compatible / santuo-workbuddy | 0.7 / 1.0 / 2048 | 687932c8df552eadba18ef0376949d01b205ad3d98e9c96a1efe2b16979161a0 | True | 1 | 0 | 973 | 768 | 1741 | plan_draft_ready | 2026-11-13T09:20:37+08:00 |
| S7 | 2 | S7 | B0 | 0 | graduation-memory-ablation@20261112T210000@b0-remainder-20261113T013105Z | b0-remainder-20261113T013105Z | openai_compatible / santuo-workbuddy | 0.7 / 1.0 / 2048 | 687932c8df552eadba18ef0376949d01b205ad3d98e9c96a1efe2b16979161a0 | True | 1 | 0 | 973 | 824 | 1797 | plan_draft_ready | 2026-11-13T09:31:32+08:00 |
| S7 | 3 | S7 | B0 | 1 | graduation-memory-ablation@20261112T210000@b0-remainder-20261113T013105Z | b0-remainder-20261113T013105Z | openai_compatible / santuo-workbuddy | 0.7 / 1.0 / 2048 | 687932c8df552eadba18ef0376949d01b205ad3d98e9c96a1efe2b16979161a0 | True | 1 | 0 | 973 | 732 | 1705 | plan_draft_ready | 2026-11-13T09:31:37+08:00 |
| S7 | 4 | S7 | B0 | 2 | graduation-memory-ablation@20261112T210000@b0-remainder-20261113T013105Z | b0-remainder-20261113T013105Z | openai_compatible / santuo-workbuddy | 0.7 / 1.0 / 2048 | 687932c8df552eadba18ef0376949d01b205ad3d98e9c96a1efe2b16979161a0 | True | 1 | 0 | 973 | 779 | 1752 | plan_draft_ready | 2026-11-13T09:31:41+08:00 |
| S7 | 5 | S7 | B0 | 3 | graduation-memory-ablation@20261112T210000@b0-remainder-20261113T013105Z | b0-remainder-20261113T013105Z | openai_compatible / santuo-workbuddy | 0.7 / 1.0 / 2048 | 687932c8df552eadba18ef0376949d01b205ad3d98e9c96a1efe2b16979161a0 | True | 1 | 0 | 973 | 991 | 1964 | plan_draft_ready | 2026-11-13T09:31:47+08:00 |

## 一致性小结

- S5：5 份 `prompt_sha256` 唯一值数量 = 1（1676ec368b81…），与设计「同格同一 Prompt」一致。
- S7：5 份 `prompt_sha256` 唯一值数量 = 1（687932c8df55…），与设计「同格同一 Prompt」一致。

## 文件与身份

- S5 第 1 次：`experiments/graduation/runs/20261112T210000-20261113T011751Z/results.jsonl`
- S7 第 1 次：`experiments/graduation/runs/20261112T210000-20261113T012031Z/results.jsonl`
- S5、S7 第 2–5 次：`experiments/graduation/runs/b0-remainder-20261113T013105Z/results.jsonl`
- 三份 `experiment_id` 互不相同；原始 `repeat_index` 在各自 run-dir 内唯一，跨 run-dir 只在「第 n 次」列统一。
- 本批次共 10 份生成（每样本 5 份），每次生成 1 次模型请求、0 次修正，全部 success=true。
