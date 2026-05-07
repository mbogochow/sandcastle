---
"@ai-hero/sandcastle": patch
---

Add GitLab Issues as a backlog manager option during init. Mirrors the GitHub Issues experience: filters by the `Sandcastle` label (with the same opt-in label-creation prompt), normalizes list output via `jq`, and posts a "Completed by Sandcastle" note when closing an issue.

`Sandcastle` label support is now declared per backlog manager via a `sandcastleLabel` field on `BacklogManagerEntry` (provider display name + label-creation shell command). `sandcastle init` consumes this generically, so adding label support to a future backlog manager is a single registry edit with no `cli.ts` changes.
