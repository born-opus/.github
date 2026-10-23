---
name: App release
about: Every step for one version of an app, from the release pull request to the App Store
title: "<App> <version>"
labels: release
---

<!-- One issue per version. Tick each step as it's done; a step that doesn't apply gets a line saying why. -->

## Release pull request

- [ ] Made with `/release` on `chore/release-<version>`, or the app's own release steps: the version, the
      changelog's Unreleased named for it, and What's New (majors and minors). Xcode Cloud numbers the builds
- [ ] Checks (GitHub Actions) and Xcode Cloud's Pull Request workflow pass
- [ ] OpusKit is on its latest release (`/update-kit`), or the pull request says why not
- [ ] If the app uses Born Opus's AI: its prompt hash is listed in opus-ai's `src/apps.ts`, and opus-ai is deployed
      to production
- [ ] If the app syncs with iCloud: the CloudKit schema is deployed from Development to Production, if a record
      type or field changed
- [ ] The privacy manifests and App Store Connect's App Privacy answers still match what the app collects
- [ ] The app's Privacy Policy and Terms on bornopus.com are republished, if they changed

## TestFlight

- [ ] The release pull request is merged, and Xcode Cloud's TestFlight workflow built and uploaded it (or
      `scripts/upload-testflight.sh <build number>` did, if Xcode Cloud couldn't or isn't set up for the app yet)
- [ ] Processed in App Store Connect and given to the internal group
- [ ] Installed over the last version on an iPhone, and an Apple Watch if the app has one: What's New shows once,
      and data is kept
- [ ] Given to external testers (Beta App Review, once per version), if they're testing this one

## App Store

- [ ] Screenshots retaken for anything that looks different
- [ ] The App Store's What's New text written from the changelog
- [ ] Review notes say how to sign in and try anything behind it
- [ ] Submitted for review, with phased release on and released by hand after approval
- [ ] The submitted build's commit, named on its Xcode Cloud build page, tagged `<version>+<build>` and pushed
- [ ] The roadmap's Done list says when it went live
