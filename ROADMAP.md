# 24-week roadmap

Assumes about 8 to 10 hours per week on top of live classes. Follow your instructor's pace for module order; shift weeks if the batch moves faster or slower. Each phase ends with a **proof**: something public in this repo.

| Weeks | Course module(s) | Learn | Build | Proof |
|---|---|---|---|---|
| 0-1 | Setup | Python 3.12, venv/uv, Git workflow, Docker basics, API-key hygiene | This repo, `.gitignore`, pre-commit with secret scanning | Repo live, first commit |
| 1-3 | 1 Intro to GenAI, 2 Prompt Engineering | Tokens, context, embeddings, RAG vs fine-tune, CoT, ReAct, few-shot, hallucination control | **01** ops prompt library (incident, Terraform review, K8s debug, cost) plus an eval set of 10 real cases | Prompt library + A/B results table |
| 3-6 | 3 GenAI on Cloud, 4 Text generation | Bedrock (Converse API), Azure AI Foundry, Vertex/Gemini; structured output; function calling | **02** CLI that takes `kubectl describe`/logs and returns ranked hypotheses via Bedrock; same task ported to Gemini and Azure | CLI + 3-cloud comparison table (cost, latency, quality) |
| 6-9 | 5 Advanced RAG | Chunking, embeddings, vector DBs (FAISS, Qdrant, Chroma), hybrid search, LangChain vs LlamaIndex, Bedrock Knowledge Bases | **03** RAG assistant over MJ's Cart docs, runbooks and incident notes, with citations | Demo + retrieval eval report |
| 9-11 | 6 Multimodal, 7 Fine-tuning | When NOT to fine-tune; LoRA/QLoRA, quantization concepts; screenshot understanding | **04** decision memo (prompt vs RAG vs fine-tune), optional small LoRA experiment, screenshot-to-diagnosis demo | Memo with cost-benefit table |
| 11-16 | 8 Agentic AI | LangGraph (state, HITL, checkpoints), MCP, A2A, Bedrock Agents / AgentCore, ADK, tool design | **05** ops agent: read-only MCP server for kubectl/AWS, LangGraph supervisor, approval gate before any change | Recorded demo + threat model |
| 16-19 | 9 Monitoring and evaluation, 10 Responsible AI | LLM-as-judge, regression tests, RAG evals, tracing (LangSmith/OTel), Bedrock Guardrails, prompt-injection defense | **06** add evals, tracing and guardrails to projects 02, 03, 05; red-team 20 injection cases | Eval dashboard + red-team report |
| 19-24 | 11 Production deployment, 12 MLOps/tools | Docker/Compose, EKS or kOps, ECR, CodeBuild/GitHub Actions, Terraform, Lambda/ECS options, LLMOps pipeline, cost controls | **07** deploy 02, 03, 05 as services with CI/CD, Prometheus/Grafana, budgets and alarms; **08** capstone integration | Live URL, architecture diagram, runbook, cost report |

## Parallel tracks (every week)
- **FDE track (2 hrs):** one customer-style scenario per week: discover, scope, demo. See [docs/fde-skills.md](docs/fde-skills.md).
- **Write-up (1 hr):** a short blog or README section per project: problem, design, trade-offs, what failed.
- **AIOps baseline (optional, weeks 16-19):** before trusting an LLM with alerts, build the classic version in [project 09](projects/09-anomaly-detection-alert-correlation/README.md) and compare. See [docs/aiops](docs/aiops/README.md).
- **Interview drills (1 hr, from week 8):** AI system design, debugging, behavioral. See [docs/interview-prep.md](docs/interview-prep.md).

## Milestones
- Week 6: first cloud GenAI tool working end to end
- Week 11: RAG assistant demo-able to a non-engineer
- Week 16: agent with approval gates and a threat model
- Week 24: capstone live, repo polished, applications going out
