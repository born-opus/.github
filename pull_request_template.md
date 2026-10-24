## Summary

<!-- One or two lines: what changes for the person using the app, or for the apps when this is OpusKit or a server. -->

## What changed

<!-- The main changes, a line each, saying where. -->

-

## Evidence

<!-- Anything people can see: screenshots in light and dark, before and after for a change, and the device or
simulator they're from. Anything else: the test or command that shows it works. -->

| Before | After (light) | After (dark) |
| --- | --- | --- |
|  |  |  |

## Checks

<!-- Tick what applies; leave out the rest. -->

- [ ] Tests pass, and the version check (`scripts/check-versions.sh`) where the repository has one
- [ ] Checked in the simulator in light and dark, then on an iPhone
- [ ] People will notice: the version raised with `/opus:release`, with its section in `CHANGELOG.md`, and the
      roadmap updated
- [ ] The app keeps something new: demo examples of it in the app's Demo Data
- [ ] Words follow OpusKit's copy rules
- [ ] The app's AI prompt or tools changed: the new hash is listed in opus-ai's `src/apps.ts` and deployed
- [ ] A synced record type or field changed: the CloudKit schema is deployed to Production before the next build
- [ ] Something another app could use: it's in OpusKit, not in the app
- [ ] An OpusKit change: every app still builds, and a visual change was agreed first, since every app takes it on
