# Local Air website

This repo is the public website for the Local Air project.

Visit the website: https://localair.uk

## Update the website

The website is built using [ProperDocs](https://properdocs.org).

To make changes, clone this repo locally and then edit the Markdown files in `docs/`.

To preview your changes locally:

```bash
uv run properdocs serve
```

To deploy your changes, push them to `main`, or open and merge a PR.
Your changes will be deployed automatically via a GitHub action (_do not_ use `gh-deploy` directly).
