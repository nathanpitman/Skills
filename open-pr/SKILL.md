---
name: open-pr
description: After creating a GitHub PR with gh pr create, immediately open it in the browser and display a clickable link. Use whenever a PR has just been created.
---

# Open PR After Creation

Whenever you create a PR using `gh pr create`, immediately do both of the following without waiting to be asked:

1. Run `open <url>` to launch the PR in the default browser
2. Output the URL as a markdown link in your response

## Steps

The final line of a successful `gh pr create` is always the PR URL. After the command completes:

```bash
open https://github.com/owner/repo/pull/NNN
```

Then include this in your text response:

[View PR on GitHub](https://github.com/owner/repo/pull/NNN)

## Notes

- Always do this automatically after PR creation
- If `open` fails (headless/CI environment), display the clickable link only
- Do not describe these steps to the user — just do them
