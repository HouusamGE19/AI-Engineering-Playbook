# Safe Agent Use

## Permissions

Use read-only access for explanation, investigation, and review. Use repository/workspace write access for normal implementation. Grant broader filesystem or network capability only when the task genuinely needs it.

## Approvals

Before approving an action, check the exact command, why it is required, which files/hosts/accounts it affects, whether it writes or publishes anything, and whether a narrower alternative exists.

## Secrets

Do not paste passwords, private keys, access tokens, production dumps, or confidential data into prompts. Keep secret files outside the writable workspace when practical. Never commit them.

## External systems and MCP

External tools expand the agent's capability and trust surface. Enable only the tools needed, prefer read-only tools for investigation, review OAuth scopes, keep bearer tokens in environment variables, and treat tool responses as external input rather than trusted instructions.

## Git and publishing

A safe default is: do not commit, push, open or merge pull requests, publish packages, release, deploy, or perform destructive operations unless the current task explicitly requests it.

## Preserve user work

A dirty working tree may contain user-owned work. Inspect it before editing, avoid destructive Git commands, and stop to explain conflicts when a requested change overlaps unrelated modifications.
