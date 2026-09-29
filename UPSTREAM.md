# Upstream and issue review

Base: [jridgewell/resolve-uri](https://github.com/jridgewell/resolve-uri), npm `@jridgewell/resolve-uri@3.1.2`, commit `caa7a299d6c688570773c81732f77d3c7035ded6`. Full Git history and upstream attribution are retained. Last npm publication: 2024-02-14T19:32:38.143Z. Release inactivity does not by itself prove abandonment.

Review: 2026-09-29T00:21:55.224783+00:00. Source coverage: Most recently updated 100 open and 30 closed issue/PR entries; PRs removed. This is triage evidence, not a claim of exhaustive review.

Open #110 asks about percent-encoding semantics: preserve input bytes and document that filesystem paths/escaping must be normalized by callers. #108 requests Windows filesystem path support beyond URI resolution; do not reinterpret backslashes or drive letters and silently change existing URI semantics. #124 asks about upstream support and #92 is a development dashboard; this independent fork makes no upstream support claim. Closed #113 query propagation is covered by the upstream suite. Closed #117 concerns using URL instead; preserve support for relative/non-absolute bases. Runtime TypeScript source is unchanged; modern build/test tools reproduce CJS/UMD, ESM and types.

## Reviewed issue entries

- [jridgewell/resolve-uri#92](https://github.com/jridgewell/resolve-uri/issues/92) (open): Dependency Dashboard
- [jridgewell/resolve-uri#124](https://github.com/jridgewell/resolve-uri/issues/124) (open): End Of Life Question
- [jridgewell/resolve-uri#110](https://github.com/jridgewell/resolve-uri/issues/110) (open): percent-encoding
- [jridgewell/resolve-uri#108](https://github.com/jridgewell/resolve-uri/issues/108) (open): Support windows paths on windows, both absolute and relative
- [jridgewell/resolve-uri#117](https://github.com/jridgewell/resolve-uri/issues/117) (closed): why not simply use URL?
- [jridgewell/resolve-uri#113](https://github.com/jridgewell/resolve-uri/issues/113) (closed): Query params need to be propagated
