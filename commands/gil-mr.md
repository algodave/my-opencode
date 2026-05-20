---
description: Open a GitLab Merge Request
---

A GitLab issue reference can optionally be provided as argument, here its value: $1
When present, such value will follow one of these 2 formats:
- <project_name>#<issue_number>
- <group_name>/<project_name>#<issue_number>

Following is the steps to perform.

1. If a GitLab issue reference is provided, parse its value and use the `glab` command to fetch issue contents, then read and understand those.
2. Look at the commits in the current branch that sit on top of the `main` branch.
3. For each commit, read and understand both the message and the changes.
4. Get a "big picture" understanding of the whole set of changes done in the current branch.
5. Figure out proper title and description for a GitLab Merge Request: title must be concise and meaningful, description must still be concise but also explanatory and structured. Use GitLab-flavored markdown to the purpose. Include reference to issue "$1" (if any) at the very beginning of description; use "Related to" rather than "Closes".
6. Push the branch to the `origin` remote, if it was not pushed yet.
7. Create the MR using the `glab` command.
