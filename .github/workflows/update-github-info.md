---
name: update-github-info
description: Agentic workflow to update GitHub info and open a PR for Mona
on:
  schedule:
    - cron: '0 9 * * *'
  workflow_dispatch: {}
tools:
  edit: true
safe-outputs:
  create-pull-request:
network:
  allowed:
    - github.com
    - github.blog
---

# Instructions

Read `notes/mona-notes.md` before making changes.

Use these sources:
- `notes/mona-notes.md`
- GitHub Blog: https://github.blog/latest/
- GitHub Changelog: https://github.blog/changelog/

Update `site/content/github-info.md` with concise,
practical updates for readers and include source context when content comes
from the GitHub Blog or GitHub Changelog.

Open a pull request for Mona to review. 
Use a pull request title that mentions Mona or GitHub Info. 
Do not write directly to `main`;
rely on `safe-outputs` with `create-pull-request`.
