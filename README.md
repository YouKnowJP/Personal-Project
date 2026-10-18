# Personal-Project

[![Switchback CI](https://github.com/YouKnowJP/Personal-Project/actions/workflows/human-game.yml/badge.svg)](https://github.com/YouKnowJP/Personal-Project/actions/workflows/human-game.yml)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

A collection of my personal software projects and experiments. Each project lives
in its own directory with its own README, setup instructions, and development notes.

## Projects

| Project | Description | Built with |
| --- | --- | --- |
| [Switchback](Switchback/README.md) | Browser Snake game with phase-switching puzzles, a campaign, and arcade modes. | JavaScript, HTML, CSS, Canvas |

Open a project's README for its requirements, run instructions, tests, and roadmap.

## Get started

Clone the repository and choose a project:

```sh
git clone https://github.com/YouKnowJP/Personal-Project.git
cd Personal-Project
```

Switchback currently requires **Node.js 22 or newer** for development. Start it
from the repository root:

```sh
npm --prefix Switchback start
```

Open [http://127.0.0.1:4173](http://127.0.0.1:4173). No package installation or
build is required. Stop the server with Ctrl+C. See the
[Switchback README](Switchback/README.md) for gameplay, controls, and other ways
to serve it.

## Development and verification

From the repository root, run all Switchback checks and create its static build:

```sh
npm --prefix Switchback run verify
```

This checks JavaScript syntax, runs the automated tests, and packages public
assets into `Switchback/dist/`. The build output is ignored by Git. CI runs these
checks on Node.js 22, 24, and 26 on Linux, plus Node.js 24 on Windows and macOS.

For project details, see Switchback's [architecture](Switchback/docs/ARCHITECTURE.md),
[QA record](Switchback/docs/QA.md), [roadmap](Switchback/ROADMAP.md),
[changelog](Switchback/CHANGELOG.md), and [release guide](Switchback/docs/RELEASING.md).

## Repository organization

```text
Switchback/              Switchback source, README, tests, and documentation
.github/                 CI, dependency updates, and contribution templates
.editorconfig            Shared editor conventions
.gitattributes           Text normalization and binary-file handling
.gitignore               Local files, dependencies, and generated output
CONTRIBUTING.md          Development and contribution guide
SECURITY.md              Security reporting and support policy
LICENSE                  Repository license
THIRD_PARTY_NOTICES.md   Asset and dependency notices
```

New projects belong in separate named directories. Add each project to the list
above and keep its setup instructions, dependencies, tests, and documentation
inside its own folder.

## Contributing and support

Read [CONTRIBUTING.md](CONTRIBUTING.md) for setup, coding conventions, tests,
and pull requests. Use the repository's
[issue templates](https://github.com/YouKnowJP/Personal-Project/issues/new/choose)
for reproducible bugs and feature requests. For sensitive reports, follow
[SECURITY.md](SECURITY.md).

## License

This repository is licensed under the [MIT License](LICENSE), unless a project
explicitly documents a different license. Switchback includes a matching license
in its distributable package. See the
[asset and dependency notices](THIRD_PARTY_NOTICES.md) for attribution details.
