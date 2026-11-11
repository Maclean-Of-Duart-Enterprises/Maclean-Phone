# Maclean Phone 1.4.9 — Build verification

## Result

The attached 1.4.9 source was compiled directly into a signed, universal release APK. No application source, dependency versions, application ID, database schema, or existing feature behavior was changed during this build.

| Check | Result |
| --- | --- |
| Release build | Passed — `:app:assembleRelease` |
| Release fatal-lint checks | Passed — `:app:lintVitalRelease` |
| Existing unit tests | Passed — 79 tests across 22 suites; 0 failures, 0 errors, 0 skipped |
| APK signature | Verified — APK Signature Scheme v2 |
| Supplied signing key | Verified — alias `macleanphonerelease`, RSA 4096-bit |
| ZIP/native-library package alignment | Passed — `zipalign -c -P 16 4` |
| Application ID | `com.macleanofduartenterprises.phone` |
| App version | `1.4.9` |
| Version code | `20` |
| Minimum Android version | Android 8.0 / API 26 |
| Target and compile SDK | API 36 |
| Packaged native architectures | `arm64-v8a`, `armeabi-v7a`, `x86`, `x86_64` |
| APK size | 173,815,150 bytes |

## Identity and integrity

APK: `Maclean-Phone-1.4.9-universal.apk`

APK SHA-256:

```text
65bb543d3872f0e919c959e67ad8193ee7395589417d520815e4b829329c88c3
```

Signing certificate SHA-256:

```text
62ebb3c5d7d722b2e1174a4622f7593926204579084f94e11151ef606b32d136
```

This certificate matches the supplied keystore and the 1.4.8 certificate fingerprint documented in the source archive. Version code 20 is higher than the documented 1.4.8 code 19. These identity checks support an in-place update over earlier Maclean Phone releases signed with this same certificate. Do not uninstall the existing app first if you want to preserve its data. An installed copy signed with another key cannot be updated with this APK.

Input source archive SHA-256:

```text
8fc89c5b73f9a8f76bf63615ac1ac27a1f14c14114de4800c1b87efef4733f1a
```

## Build and test environment

Gradle 9.4.0; Android Gradle Plugin 9.1.0; Kotlin 2.3.10; Android SDK 36 and Build Tools 36.0.0. Compilation used a complete JDK 17. The unit-test worker used Java 21 to support Robolectric's Android API 36 runtime. Build-only network configuration was supplied outside the application source.

The initial test attempt was blocked by the test worker's Java version and runtime-download configuration. Both environment issues were corrected; the final build and full existing unit-test run completed successfully without changing app code or skipping tests.

The tests cover existing contact/CRM repository and database workflows, VCF parsing and round-trip preservation, merging, contact editor routing, calling-account selection, called-line and conference-call policies, appearance, opening-page preferences, recording preferences/audio policy, caller-risk logic, voicemail preferences, IVR configuration/routing/prompts, and license text.

The compiler emitted non-fatal deprecation/annotation warnings. Native-library stripping warnings were also emitted; the supplied libraries were retained rather than removed or replaced. Release fatal-lint checks passed. A full all-severity lint audit was not performed.

## On-device verification still required

No emulator was used. No physical Android device was connected, so installation over populated app data, live carrier/SIP/Google Voice calls, Bluetooth audio, real call recording, and touch-level UI behavior were not physically tested. Passing unit tests and packaging checks does not establish those device-specific behaviors.

The supplied 1.4.9 update includes **Settings → Call screen behavior → External-origin call screen handling**, off by default. It avoids an explicit Maclean Phone foreground launch for newly connecting/dialing cellular calls when enabled. It does not guarantee that Android or Google Voice will keep Google's own call screen visible; that requires testing on the user's device.
