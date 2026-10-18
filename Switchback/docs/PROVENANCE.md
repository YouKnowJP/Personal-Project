# Source history

Switchback was first developed under `Human Game` in
[Machine-Learning-Project](https://github.com/YouKnowJP/Machine-Learning-Project).
On 2026-10-18, its current source and game-only development history were imported
into Personal-Project. This repository’s initial commit was retained and merged
with the imported game history.

The import uses `git fast-export` restricted to `Human Game/`, followed by
`git fast-import`. It preserves the game’s file changes, author and committer
identities, timestamps, and commit messages. Commit identifiers change because
the imported trees and parent graph contain only the game component. Original
commits remain available in the source repository; no remote history was rewritten.

The source snapshot at `4f8f661709069d16b407dff759fd77be5612e9c6` and imported
snapshot have the same `Human Game` Git tree:
`665c7b241f83c13dcfa74c9df451d8084e38ba83`.

| Original commit | Imported commit |
| --- | --- |
| [7ada3f0](https://github.com/YouKnowJP/Machine-Learning-Project/commit/7ada3f0a3b2acf0ebcbf7a17ebfac0bec8278b57) | [c4d8133](https://github.com/YouKnowJP/Personal-Project/commit/c4d8133b801ead009d3373648a4eeb6041557aaa) |
| [a846fdd](https://github.com/YouKnowJP/Machine-Learning-Project/commit/a846fddb1f784ccc6e96ceba3a9c1946eb8f5dbb) | [8fd9820](https://github.com/YouKnowJP/Personal-Project/commit/8fd98205f5ac24c1e46a230c9222ae9268b895f9) |
| [3c1f3e9](https://github.com/YouKnowJP/Machine-Learning-Project/commit/3c1f3e9face219e32dd4eb2eaeed96170cb03e65) | [2597ded](https://github.com/YouKnowJP/Personal-Project/commit/2597ded6ccb3deb1cc60b073f2bd583b94963959) |
| [4f8f661](https://github.com/YouKnowJP/Machine-Learning-Project/commit/4f8f661709069d16b407dff759fd77be5612e9c6) | [a21e5d4](https://github.com/YouKnowJP/Personal-Project/commit/a21e5d47057a28b656648ce543246532f6298c23) |

The migration commit then updates repository links, release metadata, the README,
license placement, and CI. The game was imported under `Human Game` and now lives in `Switchback`. Its
simulation and save format are unchanged. Other projects and assets from the original repository
were not imported. Earlier game documentation remains in the imported history.
