# AI Engineering Playbook

**Practical patterns for using coding agents as engineering tools rather than black boxes.**

I am a Java full-stack developer. This repository documents the repeatable workflow I use with coding agents such as **Codex and Hermes** for repository exploration, implementation, debugging, review, verification, and cross-stack work.

The goal is not “prompt tricks.” The goal is **reliable agent-assisted software engineering**: clear outcomes, evidence-first investigation, focused patches, explicit verification, least-privilege tool use, diff review, and human ownership of consequential actions.

## What this repository demonstrates

- Task decomposition and prompt design.
- Working effectively in unfamiliar repositories.
- Durable repository guidance with `AGENTS.md`.
- Diagnose-before-fix workflows.
- Focused implementation and regression control.
- Proportional testing and verification.
- Git/diff review of agent-generated changes.
- Safe permissions, secrets, MCP/tool usage, and external actions.
- Context management and selective parallel/subagent work.
- Screenshot-driven UI iteration.
- Clear handoff and definition-of-done practices.

## My field manual

📘 [Using Codex CLI Effectively](book/Using-Codex-CLI-Effectively.pdf)

The included manual is my practical reference for safe, reliable Codex CLI use in real repositories.

## Repository map

```text
.
├── README.md
├── AGENTS.example.md
├── book/
│   └── Using-Codex-CLI-Effectively.pdf
├── case-studies/
│   └── HED-SPACE.md
├── prompts/
│   ├── 01-understand-unfamiliar-repo.md
│   ├── 02-diagnose-before-fix.md
│   ├── 03-implement-feature.md
│   ├── 04-review-generated-work.md
│   └── 05-screenshot-ui-iteration.md
├── security/
│   └── SAFE-AGENT-USE.md
└── workflows/
    └── DAILY-WORKFLOW.md
```

## Core principle

A coding agent can inspect, edit, run commands, and accelerate feedback loops. The developer still owns the outcome. Consequential changes, publishing, deployment, destructive operations, credentials, and production actions should remain deliberate human decisions.

## Portfolio case study

[`case-studies/HED-SPACE.md`](case-studies/HED-SPACE.md) describes how I used agent-assisted engineering to work on a Tauri/Rust desktop application outside my primary Java/Spring/Angular stack.

## Primary stack

My core engineering background remains **Java, Spring Boot, Angular, SQL, and DevOps**. This playbook documents an additional skill: using modern coding agents to become effective quickly in unfamiliar systems without pretending that generated code removes the need for understanding, review, testing, or accountability.
