# Diagnose before fixing

```text
Diagnose the reported failure, but do not edit files.

Reproduce it if a safe local reproduction exists. Trace the responsible path,
identify the root cause with file references, and distinguish evidence from
inference. Propose the smallest safe fix and the regression test or validation
that would prove it.
```

After the cause is established, authorize implementation in a separate follow-up. This creates a clean distinction between discovering a problem and deciding to change code.
