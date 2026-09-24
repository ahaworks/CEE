# CEE Architecture Snapshot 01 — Public Proof

## Scope

This repository is a provenance record only. The corresponding private
snapshot contains the original CEE production source, Benchmark v2
Runner/Script/Results, retained first-pass results, and architecture/testing
contracts. None of those original files are uploaded here.

The public files are limited to:

- this proof and README;
- the SHA-256 manifest of the private snapshot;
- the final SHA-256 of that manifest;
- the OpenTimestamps proof for the manifest (`MANIFEST.sha256.ots`);
- commit/date anchors and a non-reconstructive Benchmark v2 summary.

## Snapshot integrity

- Snapshot ID: CEE Architecture Snapshot 01
- Final SHA-256 of MANIFEST.sha256:
  8d0accc8d3d1deacb87edb90eebf67e6cd1ab28fb0b41d4c20d8be883bca70b6
- The final hash is also stored in MANIFEST.sha256.final.sha256.
- The manifest lists 27 private payload files. The manifest and its final-hash
  sidecar are excluded from that payload list to avoid recursive hashing.

## Card Git evidence

The earliest direct CEE-core evidence identified in Card history is:

| Role | Commit | Date | Subject |
|---|---|---|---|
| Earliest production KnowledgeResolver + EvidenceEngine pair | 09cc8301bb27aa6a1aff657596f445839d6e1fdf | 2026-06-30T02:05:51+08:00 | Stabilize Card AI knowledge pipeline |
| Earliest inspected canonical-entity resolver evidence | 3a61475277abf4d542f06e5c720aa73b2aacfc68 | 2026-06-30T21:46:05+08:00 | Record knowledge strategy reset |
| Named target/arbitration contract expansion | c4945221ff4343480b5ef36f4e3672399abba707 | 2026-08-05T21:18:48+08:00 | feat: complete generic research fact verification |
| Production base used by Benchmark v2 | 51aea3a1a97f1ebd895fa45dca92f1528705ee16 | 2026-08-21T23:57:19+08:00 | feat: complete knowledge maintenance |
| Retained first-pass Benchmark lineage | 5cb8eb7c5d0b1c559feb9185dc9eb9c64f4b1426 | 2026-09-22T14:46:02+08:00 | test: add CEE benchmark harness and results |
| Benchmark v2 harness commit | 0f8b1bcf66007feeabf8182d1c01aebe2492ed36 | 2026-09-22T15:56:20+08:00 | test: correct CEE benchmark second pass harness |

The earliest direct claim is based on reverse history searches for concrete production symbols. In the current Card checkout, these symbols are defined in `CardApp/Data/KnowledgeProvider.swift`. The historical commit anchor is commit 09cc8301..., whose commit tree contains both `KnowledgeResolver` and
EvidenceEngine. The later c4945221... commit contains
KnowledgeQuestionFactTarget, KnowledgeQuestionFactTargetBuilder, and
EvidenceArbitrationStatus.

## Benchmark v2 public summary

- Execution model: Luna Max. Codex thinking time was not included in CEE
  latency.
- Phase A: 32 fixed synthetic Evidence-contract cases, three deterministic
  normal passes, 100 measured runs per case, 10 warm-up runs per case; 9,600
  normal samples.
- Normal aggregate p50 / p95 / p99 / mean / min / max:
  68.596666 / 128.152750 / 138.522791 / 66.554859 / 17.526792 /
  149.046250 ms.
- Contract quality: Verdict Accuracy 32/32; Selected Statement Accuracy
  19/19; Conflict Recall 5/5; Insufficient Recall 8/8; complete False
  Certainty Rate 0/13.
- Corrected Phase B CEE Core share (KnowledgeResolver plus
  EvidenceEngine) was 0.926102 of the deterministic timing slice.
- Process-level offline enforcement: PASS using a macOS sandbox-exec profile
  with deny network*; no system Wi-Fi, VPN, or network settings were changed.
- Offline aggregate p50 / p95 / p99 / mean:
  68.547041 / 128.788042 / 138.390208 / 66.797204 ms; judgment differences
  versus normal: 0, exact match: true.
- Repeatability warning: false (normal p50 range fraction 0.002572).
- Jev: skipped under Test Plan 02; no Jev API call or adapter was used.

These are synthetic contract results, not an open-world factual accuracy
claim, and the Phase B slice is not a full network/UI user journey.

## Change boundary and timestamp status

- Card production source was not modified for Benchmark v2.
- No special benchmark cache, favorable sample selection, or CEE algorithm
  change was used.
- OpenTimestamps proof: `MANIFEST.sha256.ots` is publicly available. It was
  verified with the official OpenTimestamps web verifier (PASS) against Bitcoin
  block 968259, attesting that the manifest with SHA-256
  `8d0accc8d3d1deacb87edb90eebf67e6cd1ab28fb0b41d4c20d8be883bca70b6`
  existed no later than 2026-09-23 CST.
