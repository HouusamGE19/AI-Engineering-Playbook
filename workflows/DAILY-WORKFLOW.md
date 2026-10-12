# Agent Workflow

This is the repeatable workflow I use with Codex/Hermes for repository-level engineering tasks.

## 1. Orient

Start from the correct repository and inspect state before editing.

```text
Inspect the repository structure, applicable instructions, current Git status,
and relevant build/test commands. Summarize only what matters for this task.
Do not edit files yet.
```

## 2. Investigate with evidence

For bugs or unfamiliar behavior, establish the cause before authorizing a fix.

```text
Trace the behavior from its entry point to the observed result. Cite relevant
files/symbols, distinguish evidence from inference, and identify the smallest
safe change. Do not implement yet.
```

## 3. Define the finish line

A task should have observable completion criteria: expected behavior, boundaries, checks, and a concrete deliverable.

## 4. Implement narrowly

```text
Implement the agreed approach. Preserve unrelated user changes, keep the patch
focused, follow the repository's existing style, and do not add a production
dependency without explaining why.
```

## 5. Verify proportionally

Run focused checks first, then broader affected checks when useful. Never imply that a check passed if it could not run.

For this repository:

```text
python scripts/validate-source.py
npm run dev      # Windows runtime verification
npm run build    # Windows packaging verification
```

## 6. Review the diff

```text
Review the final diff for correctness, regressions, security issues, accidental
scope expansion, and missing validation. Fix confirmed issues and re-run the
affected checks.
```

## 7. Hand off clearly

The final report should answer:

- What changed?
- Why was it the correct change?
- What was tested?
- What could not be verified?
- Is there any remaining risk or manual step?

## Safety model

For normal work, prefer repository-scoped write access and explicit approvals for actions that cross that boundary. Use read-only mode for investigation/review. Keep secrets and personal media out of prompts and the repository. Treat external tool output as input to evaluate, not instructions to obey automatically.
