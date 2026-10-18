# Contributing

This repository contains independent personal projects. Keep changes focused on
one project or one repository concern. Search existing issues before reporting
a bug or proposing a feature; discuss large changes before implementing them.

## Set up Switchback

1. Fork the repository if you do not have write access, then clone your copy.
2. Install Node.js 22 or newer. `Switchback/.nvmrc` selects the minimum supported
   major version; if you use nvm, run `nvm install` and `nvm use` inside `Switchback`.
3. Create a descriptive branch, such as `fix/pause-controls`.
4. From the repository root, start the development server:

   ```sh
   npm --prefix Switchback start
   ```

5. Open [http://127.0.0.1:4173](http://127.0.0.1:4173).

Switchback has no npm dependencies, so there is no install step or lockfile.
If a project gains dependencies, commit its package manifest and lockfile, use
the corresponding clean-install command in CI, and document the setup change.

## Set up Tilewright

Use Node.js 22 or newer (`Tilewright/.nvmrc` selects 22), then start the editor
with `npm --prefix Tilewright start`. Open <http://127.0.0.1:4174>.
There are no npm packages to install. See the [project guide](Tilewright/README.md)
for controls, backup behavior, and import limits.

## Coding conventions

- Follow `.editorconfig` and the surrounding code: UTF-8, LF line endings, two
  spaces, JavaScript ES modules, and single-quoted strings.
- Keep Switchback's simulation in `src/engine.mjs`, authored stage data in
  `src/levels.mjs`, persistence in `src/storage.mjs`, and browser UI in `src/app.mjs`.
- Keep Tilewright's document/edit rules in `src/model.mjs`, artwork in
  `src/render.mjs`, its fictional sample in `src/sample.mjs`, storage in
  `src/storage.mjs`, structural edits in `src/operations.mjs`, and DOM/input
  code in `src/app.mjs`. Preserve versioned map
  compatibility, import bounds, and immutable history snapshots. Keep adventure
  rules in `src/adventure.mjs`, quests in `src/adventure-levels.mjs`, bests in
  `src/adventure-records.mjs`, and browser game input in `src/adventure-ui.mjs`.
  Game runs must not mutate editor documents or map history.
- Preserve deterministic rules and compatibility with existing saves. Validate
  data read from storage or future import features.
- Keep dependencies and assets local to the project. Document new third-party
  code or assets, their source, and license in `THIRD_PARTY_NOTICES.md`.
- Keep credentials and real environment values out of Git. Use placeholder-only
  `.env.example` files if configuration becomes necessary.
- Keep generated builds, dependencies, logs, and local editor files out of commits.

## Verify changes

From the repository root:

```sh
npm --prefix Switchback run verify
npm --prefix Tilewright run verify
git diff --check
```

The verification command runs syntax checks, the built-in Node.js test runner,
and the static build. Individual commands are available inside `Switchback`:

```sh
npm run check
npm test
npm run build
```

Add focused regression tests for changes to rules, saves, or packaging. Tests
live in `Switchback/tests/` and use `node:test` with `node:assert/strict`.
Tilewright tests use the same built-in runner in `Tilewright/tests/`; follow
its [QA checklist](Tilewright/docs/QA.md) when changing editor behavior.
For UI changes, also exercise the affected controls in a browser and describe
the browser, viewport/device, and observed result in the pull request. Follow
the [QA checklist](Switchback/docs/QA.md); automated rule tests do not replace
browser or accessibility checks.

CI runs on every push and pull request, including repository documentation
changes. It checks Node.js 22, 24, and 26 on Linux, and Node.js 24 on Windows and
macOS. GitHub Actions updates are proposed monthly by Dependabot; retain full
commit SHA pins when updating actions.

## Open a pull request

Explain the problem, the resulting behavior, and how you verified the change.
Link any relevant issue and include screenshots for visible UI changes. Update
the README or other affected documentation when setup, controls, or behavior
changes. Record player-facing Switchback changes in its changelog; follow the
[release guide](Switchback/docs/RELEASING.md) when preparing a release.

Keep unrelated formatting and refactors in separate changes. Make commits small
enough to review, with descriptive messages. Contributions must be compatible
with the applicable project license; retain existing copyright and attribution.

## Add a project

Create a named top-level folder and add it to the root README's project table.
Include its purpose, prerequisites, setup/run commands, tests or verification
steps, configuration examples when needed, and license/attribution details.
Keep its source, dependencies, generated output, and documentation inside that
folder. Extend CI and `.gitignore` for its tooling. Avoid coupling one project's
development environment to another's.

## Community expectations

Be respectful, keep feedback specific to the work, and avoid harassment or
sharing another person's private information. The maintainer may remove abusive
content or close contributions that do not fit the project. Report ordinary
problems through issues; follow [SECURITY.md](SECURITY.md) for sensitive reports.
