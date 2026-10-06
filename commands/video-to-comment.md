---
description: Extracts Transcript and Frames from a Video and posts them to a GitLab issue as a comment.
model: anthropic/claude-sonnet-5
---

The GitLab CLI tool is essential to perform this command. Request installation and abort the whole process when the `glab` command is not present and configured. Use the `find-docs` skill if you need help using the GitLab CLI.

The `agent-browser` skill is also required to perform this command. Abort and notify user if such skill is not available.

The GitLab issue reference is provided as the first argument, here its value: $1
Such value follows one of these 2 formats:
- <project_name>#<issue_number>
- <group_name>/<project_name>#<issue_number>

The video URL is provided as the second argument, here its value: $2

Move forward when both arguments are present; othwerwise, abort and notify user.

1. Navigate to $2 via `agent-browser`.
2. Download the video file and the transcript text file.
3. Use locally available tools to capture a frame for each timestamp in the transcript.
4. Post a comment to GitLab issue $1 with video title as the heading, and each timestamped transcript text followed by the captured frame. Do not repeat the captured frame when it's too similar to the previous one, and doesn't add anything new.
