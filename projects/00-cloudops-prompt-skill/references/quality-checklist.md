# Quality checklist (run before delivering)

**Clarity**
- [ ] Goal and "done" are explicit.
- [ ] A colleague with no context could run this at 3 a.m. without doubt.
- [ ] Instructions are mostly positive and sequential.

**Context and evidence**
- [ ] Environment named (prod/non-prod), cloud, account, region.
- [ ] Tool, runtime and provider versions pinned.
- [ ] Time window and timezone (UTC) stated for incident or metric work.
- [ ] Evidence is in XML tags with placeholders; model asked to cite what it used.

**Safety**
- [ ] Read-only first; mutating steps labelled.
- [ ] Dry-run, blast radius, rollback and verification required for changes.
- [ ] No secrets requested or echoed; redaction instruction present.
- [ ] Version-honesty line present (flag uncertain flags/fields, show how to verify).
- [ ] Untrusted data treated as data (injection hygiene) when pasting logs or tickets.
- [ ] Escalation or "need more data" path exists.

**Output**
- [ ] Format matches the consumer (terminal, ticket, Slack, JSON, runbook).
- [ ] Length and sections specified.
- [ ] Confidence or severity scale defined where judgments are requested.

**Proportionality**
- [ ] Not over-engineered: no chain-of-thought or examples the task does not need.
- [ ] For reasoning models: no "think step by step".

## Evaluating a prompt before trusting it
1. Collect 3 to 5 real past cases with known good answers (a past incident, a Terraform plan with a known bad change, a cost spike with a known cause).
2. Run old and new prompt on each; compare against the known answer, not on style.
3. Score: correct finding, no invented facts, unsafe commands (should be zero), usable format.
4. Re-run on a case with *missing* data; a good prompt asks for data instead of guessing.
5. Re-test after model or tool-version changes.
