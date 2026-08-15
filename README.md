<div align="center">

# Ankit Chaudhary

**Fullstack engineer** &nbsp;·&nbsp; TypeScript &nbsp;·&nbsp; Node &nbsp;·&nbsp; React &nbsp;·&nbsp; React Native &nbsp;·&nbsp; Kotlin

[![Portfolio](https://img.shields.io/badge/Portfolio-chaudharyankit.in-2f855a?style=flat-square&logo=googlechrome&logoColor=white)](https://www.chaudharyankit.in/)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Ankit%20Chaudhary-0a66c2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/ankit-chaudhary-6b5570224/)
[![Email](https://img.shields.io/badge/Email-ak0330255%40gmail.com-c5221f?style=flat-square&logo=gmail&logoColor=white)](mailto:ak0330255@gmail.com)

</div>

---

TypeScript and Node on the server, React on the web, React Native and Kotlin on mobile, and a fair amount of LLM/AI work on top of all three. Most of my open source time goes into library and emulator internals — [react-hook-form](https://github.com/react-hook-form/react-hook-form), [pino](https://github.com/pinojs/pino), and the [floci](https://github.com/floci-io/floci) local AWS/GCP emulators. On my own time I build [ArchIt](https://github.com/ankit1324/ArchIt) and [echoframe](https://github.com/ankit1324/echoframe).

---

## Open Source

> [!NOTE]
> All merged upstream. Each row is a behaviour bug in library internals — the linked PR carries the diff and its regression tests.

| Project | Fix | PR |
|:--|:--|:--|
| **[react-hook-form](https://github.com/react-hook-form/react-hook-form)**<br>`44.8k ★` | `setValue(name, value, { shouldDirty: true })` silently no-opped on a form with `disabled: true` — neither `isDirty` nor `dirtyFields` updated. Routed an explicit programmatic opt-in through `updateTouchAndDirty` and stopped `_getDirty` forcing `false` for disabled forms. | [#13594](https://github.com/react-hook-form/react-hook-form/pull/13594) |
| **[pino](https://github.com/pinojs/pino)**<br>`18.1k ★` | The browser logger shipped no `setBindings`, so bundles resolving `browser.js` threw at runtime even though the typings declared it. Implemented against Node semantics, including `transmit` and child-logger behaviour. | [#2471](https://github.com/pinojs/pino/pull/2471) |
| **[floci](https://github.com/floci-io/floci)**<br>`20.1k ★` | EC2 `ImportKeyPair` accepted a `KeyName` already present in the region, so repeated `terraform apply` runs produced duplicate key pairs. Now returns `InvalidKeyPair.Duplicate`, matching real EC2. | [#1848](https://github.com/floci-io/floci/pull/1848) |
| **[floci](https://github.com/floci-io/floci)**<br>`20.1k ★` | EC2 `DescribeKeyPairs` returned an empty list with HTTP 200 for a missing `KeyName`/`KeyPairId`, so idempotent callers skipped creating the key. Now raises `InvalidKeyPair.NotFound`. | [#1932](https://github.com/floci-io/floci/pull/1932) |
| **[floci-gcp](https://github.com/floci-io/floci-gcp)** | The GCS CORS filter allowed every origin and ignored `Access-Control-Request-Method`, and path-style (XML API) reads resolved no bucket at all. Now enforces the bucket's real CORS config on preflight and on object reads. | [#101](https://github.com/floci-io/floci-gcp/pull/101) |

---

## Projects

| | |
|:--|:--|
| **[ArchIt](https://github.com/ankit1324/ArchIt)**<br>[archit.chaudharyankit.in](https://archit.chaudharyankit.in) | Find a property on a 3D map and design the house on it in the browser.<br><sub>Next.js · TypeScript · MapLibre GL · Supabase · Clerk · Razorpay</sub> |
| **[echoframe](https://github.com/ankit1324/echoframe)** | Turns a screenshot, its source app and URL into a searchable note. Read entirely on-device — no network access by design.<br><sub>Kotlin · Jetpack Compose · Room · ML Kit</sub> |

---

## Stack

| | |
|:--|:--|
| **Languages** | TypeScript, JavaScript, Kotlin |
| **Web** | React, Next.js, Tailwind, MapLibre GL |
| **Server** | Node.js, Express, Supabase |
| **Mobile** | React Native, Expo Router, Android, Jetpack Compose, Room, ML Kit |
| **Tooling** | Jest, GitHub Actions, ESLint |
