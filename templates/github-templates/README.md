# GitHub issue templates

These are ready-to-use GitHub issue templates. Copy them into your project's `.github/ISSUE_TEMPLATE/` directory and GitHub will offer them when someone clicks "New Issue".

## What's here

- **`epic-template.md`** — for creating an epic (a group of related work).
- **`card-template.md`** — for creating a story/card (one unit of work).

## How to use

1. Create `.github/ISSUE_TEMPLATE/` in your project repo if it doesn't exist.
2. Copy both files into it.
3. Edit the `labels:` line in the frontmatter to match labels you actually have.
4. Commit and push. GitHub will pick them up automatically.

## Filling in the cards

The templates give you the *shape*. For the actual content, either:

- Copy from `../markdown/` (or from `examples/ag-bot-cv/` for a filled-in example) into the issue body when creating it, or
- Use the `gh` CLI to bulk-create issues from the markdown files:
  ```bash
  for f in templates/markdown/01-pipeline/[0-9]*.md; do
    gh issue create --title "$(head -n1 $f | sed 's/^# //')" --body-file "$f" --label pipeline
  done
  ```
