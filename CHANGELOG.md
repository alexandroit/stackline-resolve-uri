# Stackline changes

## 1.0.0 — 2026-09-28

Independent maintenance fork of @jridgewell/resolve-uri 3.1.2. Preserve published API, module exports and runtime engine compatibility. Open #110 asks about percent-encoding semantics: preserve input bytes and document that filesystem paths/escaping must be normalized by callers. #108 requests Windows filesystem path support beyond URI resolution; do not reinterpret backslashes or drive letters and silently change existing URI semantics. #124 asks about upstream support and #92 is a development dashboard; this independent fork makes no upstream support claim. Closed #113 query propagation is covered by the upstream suite. Closed #117 concerns using URL instead; preserve support for relative/non-absolute bases. Runtime TypeScript source is unchanged; modern build/test tools reproduce CJS/UMD, ESM and types.

Pinned development tools, real API and packed-consumer checks, GitHub CI/CodeQL gates, exact-artifact npm provenance and immutable release evidence are added. See UPSTREAM.md for limits of issue triage.
