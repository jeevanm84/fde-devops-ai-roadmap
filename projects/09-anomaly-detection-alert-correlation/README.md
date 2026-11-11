# Project 09: Anomaly detection and alert correlation (classic AIOps baseline)

**Course module(s):** 12 (MLOps), complements 9
**Goal:** Detect anomalies in metrics and group related alerts without an LLM, then compare with an LLM-based approach on the same data.

## Deliverables
- [ ] Synthetic or lab metrics (CPU, latency, error rate) exported from Prometheus on the MJ's Cart cluster, with injected faults and known timestamps
- [ ] Simple detectors: rolling z-score, seasonal baseline, and one ML model (for example Isolation Forest)
- [ ] Alert correlation: group alerts by service, time window and dependency
- [ ] Evaluation: precision, recall and time-to-detect against the injected faults
- [ ] Comparison table: classic detector vs LLM summary of the same window (accuracy, latency, cost per run)
- [ ] Short write-up: where each approach wins

## Notes
- Use your own lab or synthetic data only. Do not use production data from any employer in a public repo.
- Keep it read-only: the output is a ranked list of suspected incidents, not an action.

## Definition of done
- [ ] Runs from a clean clone with documented steps
- [ ] Evals included
- [ ] Architecture diagram
- [ ] Write-up of trade-offs and failures
