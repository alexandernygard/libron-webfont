# Libron webfont

The [Libron](https://github.com/nicoverbruggen/libron) typeface by [Nico Verbruggen](https://github.com/nicoverbruggen), packaged as WOFF2 files plus a ready-made CSS file.

This is an unofficial repackaging of the unmodified web build (`Libron_Web.zip`) from the upstream [releases page](https://github.com/nicoverbruggen/libron/releases). The font files are not altered in any way. For issues with the font itself, use the upstream repo.

## Usage

### npm

```sh
npm install @alexandernygard/libron
```

```js
import "@alexandernygard/libron/libron.css";
```

### Straight from GitHub (no npm registry)

```sh
npm install github:alexandernygard/libron-webfont
```

Then import `libron-webfont/libron.css` (or `@alexandernygard/libron/libron.css`, depending on how your package manager names the dependency).

### CDN (jsDelivr)

```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@alexandernygard/libron@0.31/libron.css">
```

### Use the font

```css
body {
  font-family: "Libron", serif;
}
```

Four styles are included: Regular (400), Italic (400 italic), Bold (700) and Bold Italic (700 italic).

## License

The font is licensed under the SIL Open Font License 1.1. See [`LICENSE`](LICENSE) and [`COPYRIGHT`](COPYRIGHT), both copied verbatim from upstream. "Libron" is a Reserved Font Name; it is used here only because the fonts are redistributed unmodified.

## Updating to a new Libron release

1. Download `Libron_Web.zip` from the new [upstream release](https://github.com/nicoverbruggen/libron/releases) and replace the files in `fonts/` with the ones from the zip. Refresh `LICENSE` and `COPYRIGHT` from upstream `main` if they changed.
2. Open `index.html` (e.g. `python3 -m http.server`) and check that all four styles render.
3. Bump the version in `package.json` so major.minor matches upstream (e.g. v0.32 → `0.32.0`). The patch number is only for packaging fixes in this repo.
4. Commit, tag and push: `git tag v0.32.0 && git push && git push --tags`.
5. Publish: `npm publish --access public`.
