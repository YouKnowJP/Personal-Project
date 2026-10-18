# Assets and dependencies

Switchback includes original JavaScript, HTML, CSS, SVG artwork, synthesized
sound, and a screenshot of its interface. It bundles no font files, downloaded
audio, external images, datasets, models, or third-party runtime packages.
CSS font names refer to fonts already available on the player’s device.

Node.js serves the development files and runs tests. It is installed separately
and is not included in downloadable game packages. GitHub Actions used by CI
retain their own licenses.

The root MIT license and `Switchback/LICENSE` cover the game’s project code and
original interface assets. No additional third-party asset licenses are needed
for the current static package.

Tilewright includes original JavaScript, HTML, CSS, SVG branding, Canvas-drawn
pixel tiles, a fictional sample map, and a screenshot of its interface. It
bundles no external artwork, fonts, datasets, audio, or third-party runtime
packages. Palette previews and exports are drawn from the same local source.
Its project code and original assets use the root MIT license, also included
as `Tilewright/LICENSE`. Node.js and browsers are installed separately; CI
actions retain their own licenses.
