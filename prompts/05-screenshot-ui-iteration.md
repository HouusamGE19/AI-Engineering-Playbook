# Screenshot-driven UI iteration

```text
Use the attached screenshot as the current runtime state.

Goal:
Make [specific area] match [desired behavior/appearance].

Focus only on [component/section]. Preserve the rest of the layout and current
functionality. Inspect the relevant UI code first, explain the likely cause,
then implement the smallest change.

Afterward, tell me exactly what I should verify in the running application and
what screenshot would prove the result.
```

This pattern creates a tight loop: screenshot → focused diagnosis → implementation → runtime verification → targeted follow-up.
