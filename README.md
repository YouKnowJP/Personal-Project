# Personal-Project

[![Switchback CI](https://github.com/YouKnowJP/Personal-Project/actions/workflows/human-game.yml/badge.svg)](https://github.com/YouKnowJP/Personal-Project/actions/workflows/human-game.yml)
[![Tilewright CI](https://github.com/YouKnowJP/Personal-Project/actions/workflows/tilewright.yml/badge.svg)](https://github.com/YouKnowJP/Personal-Project/actions/workflows/tilewright.yml)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

A collection of my personal software projects and experiments. Each project lives
in its own directory with its own README, setup instructions, and development notes.

## Projects

| Project | Description | Built with |
| --- | --- | --- |
| [Switchback](Switchback/README.md) | Browser Snake game with phase-switching puzzles, a campaign, and arcade modes. | JavaScript, HTML, CSS, Canvas |
| [Tilewright](Tilewright/README.md) | Tile map editor and Lantern Trails puzzle adventures with six missions, adaptive hunters, dialogue/rescues, puzzle mechanics, and custom map play. | JavaScript, HTML, CSS, Canvas |

Open a project's README for its requirements, run instructions, tests, and roadmap.

## Get started

Clone the repository and choose a project:

```sh
git clone https://github.com/YouKnowJP/Personal-Project.git
cd Personal-Project
```

Both projects require **Node.js 22 or newer** for development and have no npm
dependencies. Start either project from the repository root:

```sh
npm --prefix Switchback start
# Or, for the tile map editor and Lantern Trails:
npm --prefix Tilewright start
```

Open Switchback at [http://127.0.0.1:4173](http://127.0.0.1:4173), or Tilewright at
[http://127.0.0.1:4174](http://127.0.0.1:4174). No package installation or build
is required. Stop a server with Ctrl+C. Each project's README explains its
controls, local storage, and static distribution.

## Development and verification

From the repository root, verify each project and create its static build:

```sh
npm --prefix Switchback run verify
npm --prefix Tilewright run verify
```

This checks JavaScript syntax, runs the automated tests, and packages public
assets into each project's `dist/`. The build output is ignored by Git. CI runs these
checks on Node.js 22, 24, and 26 on Linux, plus Node.js 24 on Windows and macOS.

For project details, see Switchback's [architecture](Switchback/docs/ARCHITECTURE.md),
[QA record](Switchback/docs/QA.md), [roadmap](Switchback/ROADMAP.md),
[changelog](Switchback/CHANGELOG.md), and [release guide](Switchback/docs/RELEASING.md).
Tilewright has its own [architecture](Tilewright/docs/ARCHITECTURE.md),
[QA record](Tilewright/docs/QA.md), [roadmap](Tilewright/ROADMAP.md), and
[project status and submission notes](Tilewright/docs/SUBMISSION.md).

## Repository organization

```text
Switchback/              Switchback source, README, tests, and documentation
Tilewright/              Tile map editor, adventure game, tests, and roadmap
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
explicitly documents a different license. Both projects include matching licenses
in their distributable packages. See the
[asset and dependency notices](THIRD_PARTY_NOTICES.md) for attribution details.
