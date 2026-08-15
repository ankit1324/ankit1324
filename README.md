# Ankit Chaudhary

Fullstack engineer. TypeScript and Node on the server, React on the web, Kotlin on Android, and a fair amount of LLM/AI work on top of all three.
Most of my open source time goes into library and emulator internals: [react-hook-form](https://github.com/react-hook-form/react-hook-form), [pino](https://github.com/pinojs/pino), and the [floci](https://github.com/floci-io/floci) local AWS/GCP emulators.
On my own time I build [ArchIt](https://github.com/ankit1324/ArchIt), a 3D property and home-design app, and [echoframe](https://github.com/ankit1324/echoframe), an on-device Android note assistant.

## Open Source Contributions

| Project | What the fix did | PR | Status |
|---|---|---|---|
| [react-hook-form](https://github.com/react-hook-form/react-hook-form) (44.8k ★) | `setValue(name, value, { shouldDirty: true })` never updated `isDirty`/`dirtyFields` on a form with `disabled: true`. Let an explicit programmatic opt-in through `updateTouchAndDirty`, and stopped `_getDirty` from forcing `false` for disabled forms. | [#13594](https://github.com/react-hook-form/react-hook-form/pull/13594) | Merged |
| [floci](https://github.com/floci-io/floci) (20.1k ★) | EC2 `ImportKeyPair` accepted a `KeyName` that already existed in the region, so repeated `terraform apply` runs produced duplicate key pairs. Now returns `InvalidKeyPair.Duplicate` like real EC2. | [#1848](https://github.com/floci-io/floci/pull/1848) | Merged |
| [floci](https://github.com/floci-io/floci) (20.1k ★) | EC2 `DescribeKeyPairs` returned an empty list with HTTP 200 for a missing `KeyName`/`KeyPairId`, so idempotent callers skipped creating the key. Now raises `InvalidKeyPair.NotFound`. | [#1932](https://github.com/floci-io/floci/pull/1932) | Merged |
| [pino](https://github.com/pinojs/pino) (18.1k ★) | The browser logger had no `setBindings`, so bundles resolving `browser.js` threw at runtime despite the typings declaring it. Implemented it against Node semantics, including `transmit` and child-logger behaviour. | [#2471](https://github.com/pinojs/pino/pull/2471) | Merged |
| [floci-gcp](https://github.com/floci-io/floci-gcp) | The GCS CORS filter allowed every origin and ignored `Access-Control-Request-Method`, and path-style (XML API) reads resolved no bucket at all. Now enforces the bucket's actual CORS config on preflight and on object reads. | [#101](https://github.com/floci-io/floci-gcp/pull/101) | Merged |

## Projects

- **[ArchIt](https://github.com/ankit1324/ArchIt)**: find a property on a 3D map and design the house on it in the browser. Next.js, MapLibre and Three.js, with Clerk auth and Razorpay payments. Live at [archit.chaudharyankit.in](https://archit.chaudharyankit.in).
- **[echoframe](https://github.com/ankit1324/echoframe)**: Kotlin/Android assistant that turns a screenshot, its source app and URL into a searchable note, read entirely on-device with ML Kit. No network access by design.

## Contact

[![Portfolio](https://img.shields.io/badge/Portfolio-chaudharyankit.in-4c1?style=flat-square&logo=googlechrome&logoColor=white)](https://www.chaudharyankit.in/)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Ankit%20Chaudhary-0077B5?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/ankit-chaudhary-6b5570224/)
[![Email](https://img.shields.io/badge/Email-ak0330255%40gmail.com-D14836?style=flat-square&logo=gmail&logoColor=white)](mailto:ak0330255@gmail.com)
