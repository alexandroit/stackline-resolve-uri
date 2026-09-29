# @stackline/resolve-uri

Independent maintenance fork of `@jridgewell/resolve-uri@3.1.2`. Original API, module format, runtime dependency ranges, and supported Node.js engines are preserved.

```sh
npm install @stackline/resolve-uri
# Preserve existing imports with an npm alias:
npm install @jridgewell/resolve-uri@npm:@stackline/resolve-uri@1.0.0
```

See [UPSTREAM.md](UPSTREAM.md) for the exact source and issue review, and [CHANGELOG.md](CHANGELOG.md) for focused maintenance changes. Development and release tooling runs on Node.js 24; that does not change the library runtime requirement.

Maintained by [Stackline](https://alexandro.net/). [Issues](https://github.com/alexandroit/stackline-resolve-uri/issues) · [npm](https://www.npmjs.com/package/@stackline/resolve-uri).

## Upstream documentation

# @jridgewell/resolve-uri

> Resolve a URI relative to an optional base URI

Resolve any combination of absolute URIs, protocol-realtive URIs, absolute paths, or relative paths.

## Installation

```sh
npm install @jridgewell/resolve-uri
```

## Usage

```typescript
function resolve(input: string, base?: string): string;
```

```js
import resolve from '@jridgewell/resolve-uri';

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
