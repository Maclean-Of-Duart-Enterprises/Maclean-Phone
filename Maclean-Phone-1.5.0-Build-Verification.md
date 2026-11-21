# Maclean Phone 1.5.0 — Build verification

## Result

Built the attached `Maclean-Phone-1.5.0-Source.zip` directly into a signed universal release APK. No application source or dependency versions were changed during this build. The source already specified version 1.5.0, version code 21.

| Check | Result |
| --- | --- |
| Release build | Passed — `:app:assembleRelease` |
| Release fatal-lint checks | Passed — `:app:lintVitalRelease` |
| Existing unit tests | 79 passed across 22 suites; 0 failures, 0 errors, 0 skipped |
| APK signature | Verified — APK Signature Scheme v2 |
| Signer | Existing release key, alias `macleanphonerelease`, RSA 4096-bit |
| APK package/native-library ZIP alignment | Passed — `zipalign -c -P 16 4` |
| Application ID | `com.macleanofduartenterprises.phone` |
| Version name / code | `1.5.0` / `21` |
| Minimum Android version | Android 8.0 / API 26 |
| Target / compile SDK | API 36 / API 36 |
| Native architectures | `arm64-v8a`, `armeabi-v7a`, `x86`, `x86_64` |
| APK size | 173,815,150 bytes |

## Signing and upgrade compatibility

Certificate SHA-256:

```text
62ebb3c5d7d722b2e1174a4622f7593926204579084f94e11151ef606b32d136
```

The verified certificate is the same release identity used for the 1.4.9 build in this conversation. The application ID is unchanged, and version code increased from 20 to 21. These checks satisfy the package identity/version requirements for an in-place update over that release. Installation over populated device data was not physically tested. Do not uninstall the existing app before updating if you want to retain its data. An installed copy signed with a different key cannot be updated with this APK.

## Integrity

Output: `Maclean-Phone-1.5.0-universal.apk`

APK SHA-256:

```text
eea4157ba5410233358b2473ca35751f100be34b5bb1b40e0e0745f83b71f796
```

Input source archive SHA-256:

```text
59a8e48516c5eec9998855eb6ec2df9142c039af7449a765ce41cfc82a3c89bc
```

## Build environment and scope

Gradle 9.4.0, Android Gradle Plugin 9.1.0, Kotlin 2.3.10, Temurin JDK 21.0.13, Android SDK 36, and Build Tools 36.0.0. The source's Java/Kotlin bytecode target remains 17. Environment-specific network configuration was supplied outside the application source and was not packaged into the APK.

The existing unit-test suite ran without excluding or skipping tests. Compiler deprecation/annotation warnings, manifest-merger warnings, native-library stripping warnings, and a stale Kotlin-session warning were non-fatal. The supplied native libraries were retained. The build and release fatal-lint checks completed successfully; a separate full all-severity lint/security audit was not performed.

## Device verification still required

No emulator was used and no physical Android device was connected. Real installation/upgrade, live carrier/SIP/Google Voice calls, Bluetooth routing, call recording, and touch-level UI workflows were not physically tested. Passing the existing unit tests does not prove those device-specific behaviors.

For the supplied 1.5.0 Recents change, test on the phone: call an unknown number, save it as a contact, return to Recents, and verify that its name appears without another call. Also check a renamed contact and persistence after restarting the app. These new on-device workflows were not run here.

Known source limitation: `VERSION-1.5.0-NOTES.md` states that the Contacts-only call-log filter still uses Android's cached lookup URI. Older calls may therefore remain absent from that filter until the Android provider updates its cache. This behavior was preserved in this build, not silently modified.
