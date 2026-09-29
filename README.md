# @stackline/resolve-uri

> Resolve a URI relative to an optional base URI.

[![npm version](https://img.shields.io/npm/v/@stackline/resolve-uri.svg?style=flat-square)](https://www.npmjs.com/package/@stackline/resolve-uri)
[![license](https://img.shields.io/npm/l/@stackline/resolve-uri.svg?style=flat-square)](https://github.com/alexandroit/stackline-resolve-uri)
[![GitHub repository](https://img.shields.io/badge/GitHub-repository-181717?style=flat-square&logo=github)](https://github.com/alexandroit/stackline-resolve-uri)
[![Docs](https://img.shields.io/badge/docs-alexandro.net-0f766e?style=flat-square)](https://alexandro.net/docs/vanilla/resolve-uri/)
[![Reddit community](https://img.shields.io/badge/community-r%2FStackline-ff4500?style=flat-square&logo=reddit&logoColor=white)](https://www.reddit.com/r/Stackline/)

**[Documentation](https://alexandro.net/docs/vanilla/resolve-uri/)** | **[npm](https://www.npmjs.com/package/@stackline/resolve-uri)** | **[Issues](https://github.com/alexandroit/stackline-resolve-uri/issues)** | **[Repository](https://github.com/alexandroit/stackline-resolve-uri)**

**Current package version:** `1.0.2`

---

## Why this package?

`@stackline/resolve-uri` is the Stackline-maintained distribution of `@jridgewell/resolve-uri@3.1.2`. It is an independent continuation of [@jridgewell/resolve-uri](https://github.com/jridgewell/resolve-uri); original authors and licenses remain credited below.

## Compatibility

| Item | Value |
| :--- | :--- |
| Package | `@stackline/resolve-uri@1.0.2` |
| API target | `@jridgewell/resolve-uri@3.1.2` |
| Supported Node.js | `>=6.0.0` |
| License | `MIT` |
| Main entry | `dist/resolve-uri.umd.js` |
| Module entry | `dist/resolve-uri.mjs` |
| Types | `dist/types/resolve-uri.d.ts` |
| Runtime dependencies | `none` |

## Installation

```bash
npm install @stackline/resolve-uri
```

Preserve existing imports and plugin resolution with an npm alias:

```bash
npm install @jridgewell/resolve-uri@npm:@stackline/resolve-uri
```

## Usage and API reference

### @jridgewell/resolve-uri

> Resolve a URI relative to an optional base URI

Resolve any combination of absolute URIs, protocol-realtive URIs, absolute paths, or relative paths.

## Installation

```sh
npm install @stackline/resolve-uri
```

## Usage

```typescript
function resolve(input: string, base?: string): string;
```

```js
import resolve from '@stackline/resolve-uri';

resolve('foo', 'https://example.com'); // => 'https://example.com/foo'
```

| Input                 | Base                    | Resolution                     | Explanation                                                  |
|-----------------------|-------------------------|--------------------------------|--------------------------------------------------------------|
| `https://example.com` | _any_                   | `https://example.com/`         | Input is normalized only                                     |
| `//example.com`       | `https://base.com/`     | `https://example.com/`         | Input inherits the base's protocol                           |
| `//example.com`       | _rest_                  | `//example.com/`               | Input is normalized only                                     |
| `/example`            | `https://base.com/`     | `https://base.com/example`     | Input inherits the base's origin                             |
| `/example`            | `//base.com/`           | `//base.com/example`           | Input inherits the base's host and remains protocol relative |
| `/example`            | _rest_                  | `/example`                     | Input is normalized only                                     |
| `example`             | `https://base.com/dir/` | `https://base.com/dir/example` | Input is joined with the base                                |
| `example`             | `https://base.com/file` | `https://base.com/example`     | Input is joined with the base without its file               |
| `example`             | `//base.com/dir/`       | `//base.com/dir/example`       | Input is joined with the base's last directory               |
| `example`             | `//base.com/file`       | `//base.com/example`           | Input is joined with the base without its file               |
| `example`             | `/base/dir/`            | `/base/dir/example`            | Input is joined with the base's last directory               |
| `example`             | `/base/file`            | `/base/example`                | Input is joined with the base without its file               |
| `example`             | `base/dir/`             | `base/dir/example`             | Input is joined with the base's last directory               |
| `example`             | `base/file`             | `base/example`                 | Input is joined with the base without its file               |

## Credits and original authors

- Original project: [@jridgewell/resolve-uri](https://github.com/jridgewell/resolve-uri).
- Justin Ridgewell.
- Copyright 2019 Justin Ridgewell <jridgewell@google.com>.
- Stackline maintenance: [Alexandro Paixao Marques](https://www.linkedin.com/in/aleinfo/) and [Stackline contributors](https://github.com/alexandroit).

Original copyright, license notices and contributor acknowledgements remain part of this distribution. Stackline maintenance does not replace authorship of the original work.

## License

`MIT`. See the license and notice files in the [repository](https://github.com/alexandroit/stackline-resolve-uri).

## Community and Links

- [Stackline website](https://alexandro.net/)
- [GitHub projects](https://github.com/alexandroit)
- [npm packages](https://www.npmjs.com/~alex360qc)
- [Reddit community — r/Stackline](https://www.reddit.com/r/Stackline/)
- [Maintainer LinkedIn](https://www.linkedin.com/in/aleinfo/)

Use this repository's issue tracker for reproducible bugs and feature requests. Join r/Stackline for examples, usage questions and release discussions.
