# Maclean Phone 1.4.6 Build Verification Report

Build date: 2026-10-01

## Release identity

| Property | Verified value |
|---|---|
| Application ID | `com.macleanofduartenterprises.phone` |
| Version name | `1.4.6` |
| Version code | `17` |
| Minimum SDK | `26` |
| Target / compile SDK | `36` / `36` |
| APK type | Universal |
| Packaged ABIs | `arm64-v8a`, `armeabi-v7a`, `x86`, `x86_64` |
| APK size | 173,798,586 bytes |
| APK SHA-256 | `d20e4eeda05036c168cbd68969c97d0d333e9f64c38697e6758f1606ab813cbf` |

## Build environment and tasks

- Eclipse Temurin JDK 21.0.12.1
- Gradle 9.4.0
- Android SDK Platform 36 / Build Tools 36.0.0
- `testDebugUnitTest`: passed — 73 tests, 0 failures, 0 errors, 0 skipped
- `lintRelease`: passed — 0 errors, 62 warnings, 1 hint
- `assembleRelease`: passed

The remaining lint findings are non-blocking inherited API/deprecation, manifest-merge, resource, and dependency-modernization guidance. No lint baseline or error suppression was introduced to make this release pass.

## APK verification

- `aapt dump badging` confirms package `com.macleanofduartenterprises.phone`, version code `17`, version name `1.4.6`, minimum SDK 26, target SDK 36, and the expected phone/contact permissions.
- `apksigner verify --verbose --print-certs` passes with one APK Signature Scheme v2 signer.
- Signer subject: `CN=Maclean Phone, OU=Mobile Applications, O=Maclean of Duart Enterprises`
- Signer certificate SHA-256: `62ebb3c5d7d722b2e1174a4622f7593926204579084f94e11151ef606b32d136`
- `zipalign -c -P 16 -v 4` reports verification successful.
- Universal native libraries are present for `arm64-v8a`, `armeabi-v7a`, `x86`, and `x86_64`.

The unchanged application ID, increased version code, and unchanged signer satisfy Android's package-level requirements for an in-place update over the correctly signed 1.4.5 release.

## Upgrade and data-integrity review

- No database version or schema was changed.
- No destructive migration or clearing operation was added.
- Existing CRM contact IDs, Android contact links, groups, memberships, photos, custom fields, and sorting preferences are preserved.
- The opening-page and last-used-home-tab values use new additive SharedPreferences keys. Existing users receive **Recents** as the safe default.
- The Favorites folder queries the existing persisted CRM `favorite` field; it does not duplicate contacts or migrate them between storage providers.
- The legacy Favorites navigation key remains readable internally for restored navigation state, but it is absent from the visible bottom destinations.

## Verification boundary

Static review, JVM/Robolectric workflow tests, lint, signed packaging, package metadata, certificate, ABI, permission, and alignment checks were completed. `adb` was unavailable in the build environment, so installation over a populated 1.4.5 phone and touch-level UI behavior were not falsely marked as physically tested. The focused device checklist is in the Home Navigation and Favorites Test Report.
