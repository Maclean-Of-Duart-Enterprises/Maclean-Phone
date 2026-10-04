# Maclean Phone 1.4.6 Release Notes

Release date: 2026-10-01

## Contacts and Favorites

- Removed the separate **Favorites** destination from the bottom navigation.
- Added a starred **Favorites** filter inside **Maclean CRM Contacts**, next to **All** and the custom contact groups.
- The new filter reads the same persisted CRM favorite flag that is changed by **Add favorite** / **Remove favorite** on the contact actions dialog. This fixes the former split behavior where the old page queried Android's starred-contact provider while the CRM contact displayed its own star.
- Favorite changes refresh the contact list after the database operation succeeds. A contact removed from favorites disappears immediately while the Favorites filter is active and remains removed after restart.
- Favoriting an Android-only contact creates the required linked CRM extension without changing the underlying Android contact identity.

## Home navigation

- The bottom navigation now contains exactly two standard destinations: **Contacts** on the left and **Recents** on the right.
- Added a Settings gear to the Contacts header for direct access to application settings.
- Added **Settings → General → Default opening page** with these persistent choices:
  - **Contacts**
  - **Recents**
  - **Last used**
- **Last used** records only the two home destinations, so opening Settings or another detail screen does not replace the remembered home page.
- Existing installations default to **Recents** until the user chooses another opening behavior.

## Compatibility

- Application ID remains `com.macleanofduartenterprises.phone`.
- Version name is `1.4.6`; version code is `17`.
- The release is signed with the existing Maclean Phone signing identity and is intended to install directly over the correctly signed 1.4.5 release without uninstalling or clearing data.
- No database schema change, destructive migration, or contact rewrite was introduced.
- Existing CRM contacts, groups, photos, custom fields, sorting, call history, calling accounts, Google Voice compatibility, SIP/VoIP, caller ID, incoming called-number display, group calls, call audio routing, voicemail, forwarding, accessibility, appearance, and AGPLv3 license functionality are retained.

## Verification summary

- 73 unit and Robolectric workflow tests passed with no failures, errors, or skips.
- Release lint passed with zero errors, 62 non-blocking warnings, and one informational hint.
- Signed release assembly, package/version inspection, signature verification, zip alignment, permission inspection, and universal ABI inspection passed.
- No Android device or emulator was attached, so the included test report clearly separates automated/code-path verification from the short physical-device acceptance checklist.
