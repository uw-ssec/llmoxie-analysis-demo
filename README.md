# llmoxie-analysis

Home to the llmoxie data analysis package

## Prerequisites

This project uses [Pixi](https://pixi.sh) for dependency management and task
execution. Install Pixi by following the
[installation instructions](https://pixi.sh/latest/#installation).

## Getting Started

### Installation

Install dependencies:

```bash
# Install dependencies (Pixi will automatically create the environment)
pixi install
```

This creates the `default` environment, which includes Python, the development
tools (pytest, ruff, pre-commit, build, hatchling), the documentation tooling,
and `llmoxie-analysis` itself as an editable install.

See the [Getting Started](docs/getting-started.md) guide for more detail.

## Project Structure

This project is organized using Pixi features for modular dependency management:

- **`docs`**: MkDocs Material for building and previewing the documentation site

## Available Environments

- **`default`**: Standard development environment with the test, lint, and build
  tooling plus the `docs` feature

## Development

### Common Tasks

| Task                  | Command                   |
| --------------------- | ------------------------- |
| Run the test suite    | `pixi run test`           |
| Lint and check format | `pixi run lint`           |
| Build wheel and sdist | `pixi run build`          |
| Run pre-commit hooks  | `pixi run pre-commit-all` |
| Run the quality gate  | `pixi run verify`         |
| Preview the docs      | `pixi run docs-serve`     |
| Build the docs        | `pixi run docs-build`     |

Run `pixi task list` to see every available task with its description.

### Using the Environment

Open a shell with the environment activated:

```bash
pixi shell
```

### Adding Dependencies

Edit `pixi.toml` to add new dependencies:

```toml
[dependencies]
your-package = ">=1.0.0"
```

Then run:

```bash
pixi install
```

or

Directly add packages (this will edit the pixi toml and install):

```bash
pixi add your-package
```

## Documentation

The documentation site is plain Markdown under [`docs/`](docs/), built with
[MkDocs Material](https://squidfunk.github.io/mkdocs-material/) and configured
in [`mkdocs.yml`](mkdocs.yml).

```bash
pixi run docs-serve    # live reload at http://127.0.0.1:8000
pixi run docs-build    # build into site/, failing on any warning
```

To add a page, create a Markdown file under `docs/` and list it in the `nav:`
section of `mkdocs.yml`.

## Contributing

Please read [CONTRIBUTING.md](CONTRIBUTING.md) for details on our code of
conduct and the process for submitting pull requests.

## License

This project is licensed under the terms specified in the [LICENSE](LICENSE)
file.
