# Personal-Project

## Switchback

**Six circuits. Endless detours.** Switchback is a browser Snake game with
phase-matching gates, six authored campaign stages, playable lessons, saved route
medals, and three arcade modes. It supports keyboard, touch buttons, and swipes,
with optional synthesized sound and high contrast.

The game lives in [Switchback](Switchback/README.md). It uses vanilla JavaScript,
Canvas 2D, HTML, and CSS, with no runtime packages, accounts, or backend.

![Switchback campaign](Switchback/docs/switchback.png)

### Run locally

Node.js 22+; no dependency installation is needed.

```sh
git clone https://github.com/YouKnowJP/Personal-Project.git
cd 'Personal-Project/Switchback'
npm start
```

Open **http://127.0.0.1:4173**. Stop with Ctrl+C.

Alternatively, download the [latest release](https://github.com/YouKnowJP/Personal-Project/releases/latest),
extract it, and serve the game folder with `python3 -m http.server 4173 --bind 127.0.0.1`.

### Develop

From `Switchback`:

```sh
npm run check
npm test
npm run build
```

The build writes a standalone static game to `dist/`. GitHub Actions checks the
source, runs 42 tests, and builds the package.

[Controls and rules](Switchback/README.md) · [Roadmap](Switchback/ROADMAP.md) ·
[Architecture](Switchback/docs/ARCHITECTURE.md) · [QA record](Switchback/docs/QA.md) ·
[Releasing](Switchback/docs/RELEASING.md) · [Source history](Switchback/docs/PROVENANCE.md)

MIT; see [LICENSE](LICENSE) and the [asset notice](THIRD_PARTY_NOTICES.md).
