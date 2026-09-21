# Contributing

Contributions are welcome. The full process lives in the repository; this page
points to it and explains how to add to these docs.

## Before you start

- Read the
  [contributing guide](https://github.com/uw-ssec/llmoxie-analysis/blob/main/CONTRIBUTING.md)
  for the pull request workflow and development setup.
- Read the
  [Code of Conduct](https://github.com/uw-ssec/code-of-conduct/blob/main/CODE_OF_CONDUCT.md).

## Adding to these docs

Pages are plain Markdown files under `docs/`, rendered by
[MkDocs Material](https://squidfunk.github.io/mkdocs-material/).

1. Create or edit a Markdown file under `docs/`.
2. If the page is new, add it to the `nav:` section of `mkdocs.yml`.
3. Run `pixi run docs-build`. The build is strict, so a page missing from the
   navigation or a broken link fails it.

Start every page with a level-1 heading and a one or two sentence summary, and
use relative links between pages.
