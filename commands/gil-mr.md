---
description: Open a GitLab Merge Request
---

1. Use the `glab` command to read and understand issue "$1" (if any).
2. Look at the commits in the current branch that sit on top of the `main` branch.
3. For each commit, read and understand both the message and the changes.
4. Get a "big picture" understanding of the whole set of changes done in the current branch.
5. Figure out proper title and description for a GitLab Merge Request: title must be concise and meaningful, description must still be concise but also explanatory and structured. Use GitLab-flavored markdown to the purpose. Include reference to issue "$1" (if any) at the very beginning of description; use "Related to" rather than "Closes".
6. Push the branch to the `origin` remote, if it was not pushed yet.
7. Create the MR using the `glab` command.
