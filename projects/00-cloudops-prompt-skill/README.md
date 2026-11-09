# CloudOps Prompt Engineering Skill

An AI skill that turns a rough draft into a production-grade prompt for **cloud, DevOps, SRE, platform and operations** work. You get a ready-to-paste prompt plus a changelog of what changed and why.

Inspired by the structure of [PhAlves23/prompt-engineering-skill](https://github.com/PhAlves23/prompt-engineering-skill), but specialised for ops: evidence-first prompts, safety rails (read-only first, dry-run, rollback, no secrets), version pinning, and agent approval gates.

## Covers
Incident triage/RCA · log and metric analysis · Terraform/CloudFormation/Ansible review · Kubernetes/EKS/ECS debugging · CI/CD · runbooks · postmortems · FinOps · security/compliance · architecture · autonomous ops agents.

## Install

**Claude Code (personal skill)**
```bash
mkdir -p ~/.claude/skills
cp -r cloudops-prompt-engineering ~/.claude/skills/
```
Restart Claude Code, then say "improve this prompt for an incident triage" or run it by name.

**Claude.ai / Desktop**: upload `cloudops-prompt-engineering.skill` under Settings > Capabilities > Skills (or use the Save skill button).

## Usage examples
- "Improve this prompt: why is prod slow?"
- "Write a safe prompt for reviewing Terraform plans before apply"
- "Make an agent system prompt for an EKS ops bot with approval gates"
- "Harden this runbook-generation prompt"

## Structure
```
cloudops-prompt-engineering/
├── SKILL.md                      # workflow + principles
├── references/
│   ├── domain-patterns.md        # per-task patterns and fragments
│   ├── safety-guardrails.md      # paste-in guardrail blocks, agent approval gates
│   ├── worked-examples.md        # 7 draft -> optimized -> changelog cases
│   └── quality-checklist.md      # pre-delivery review and eval tips
└── assets/ops-prompt-template.md # canonical skeleton
```

## License
MIT
