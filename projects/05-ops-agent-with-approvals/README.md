# Project 05: Ops agent with human approval

**Course module(s):** 8
**Goal:** LangGraph supervisor agent with a read-only MCP server for kubectl and AWS, and an approval gate before any mutating action.

## Deliverables
- [ ] MCP server exposing read-only tools
- [ ] LangGraph graph with interrupt for approval and checkpointing
- [ ] Threat model: prompt injection, over-permissioned tools, loops
- [ ] Audit log of every tool call

## Notes
No standing prod credentials; short-lived scoped tokens only.

## Definition of done
- [ ] Runs from a clean clone with documented steps
- [ ] Evals included
- [ ] Architecture diagram
- [ ] Write-up of trade-offs and failures
