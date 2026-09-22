# Benchmark v2 — Public Summary

This is a non-reconstructive summary of the private CEE Architecture Snapshot
01 benchmark result.

| Item | Result |
|---|---|
| Execution model | Luna Max |
| Phase A | 32 fixed synthetic cases × 3 normal passes × 100 measured runs |
| Normal samples | 9,600 |
| Normal p50 / p95 / p99 | 68.596666 / 128.152750 / 138.522791 ms |
| Normal mean / min / max | 66.554859 / 17.526792 / 149.046250 ms |
| Verdict Accuracy | 32 / 32 |
| Selected Statement Accuracy | 19 / 19 |
| Conflict Recall | 5 / 5 |
| Insufficient Recall | 8 / 8 |
| Complete False Certainty Rate | 0 / 13 |
| Corrected Phase B CEE Core share | 0.926102 |
| Offline enforcement | PASS; process-level sandbox-exec, deny network* |
| Offline p50 / p95 / p99 / mean | 68.547041 / 128.788042 / 138.390208 / 66.797204 ms |
| Offline judgment difference | 0; exact match |
| Jev | skipped under Test Plan 02 |
| Repeatability warning | false |

The benchmark used fixed synthetic Evidence contracts and does not represent
open-world factual accuracy or full network/UI product latency.
