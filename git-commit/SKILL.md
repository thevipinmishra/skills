---
name: git-commit
description: Use when the user explicitly asks to commit existing changes. Analyze pending changes, identify files related to the requested work, and create one or more clean commits with appropriate commit messages.
---

# Git Commit

When the user explicitly asks to commit changes:

1. Inspect the current Git status and pending changes before committing.
2. Review the diff to understand what each changed file contains.
3. Identify which files are related to the requested work.
4. By default, include all changes related to the requested work.
5. Do NOT commit unrelated changes, temporary files, scratchpads, generated files, or documentation/Markdown files unless:
   - they are part of the requested change, or
   - the user explicitly asks to include them.
6. If changes contain multiple clearly independent pieces of work, split them into separate commits when doing so improves clarity.
7. Stage only the files intended for each commit.
8. Verify the staged diff before committing.
9. Create a concise, descriptive commit message based strictly on the actual code changes.
10. After committing, verify the resulting Git status.

## Commit Quality

- Follow conventional, open-source-style commit messages.
- Prefer messages that describe the change rather than the implementation process.
- Keep commit messages concise and specific.
- Do NOT include `Co-authored-by`, `Contributed-by`, `Authored-by`, or similar attribution blocks.
- Do NOT add unrelated context, explanations, or generated text to the commit message.
- Never claim changes that are not present in the commit.

## Safety

- NEVER commit or push without explicit user confirmation.
- NEVER use `git add .` or `git add -A` blindly.
- NEVER overwrite, discard, reset, or revert unrelated user changes.
- If it is unclear whether a changed file belongs to the requested work, ask the user before including it.
- Do NOT push unless the user explicitly asks for a push.
