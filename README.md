Maclean Phone

Maclean Phone is an Android cellular dialer, contacts/CRM and SIP/VoIP application developed for home and business use by Maclean Of Duart Enterprises.

| 
Current version| 1.4.9
Version code| 20
Platform| Android 8.0+ (minimum SDK 26)
Target / compile SDK| 36 / 36
Application ID| "com.macleanofduartenterprises.phone"
Source license| GNU Affero General Public License v3 (AGPLv3); see bundled notices for third-party components
Developer| Maclean Of Duart Enterprises

Features

Standard Phone and Cellular Calling

- Android default-dialer integration and system-managed cellular calls.
- Dial pad with standard dialing and in-call DTMF controls.
- Incoming, outgoing, active, held and disconnected call states.
- Answer, decline, hang up, mute, speakerphone and available audio routing controls.
- Multiple SIM / Android calling-account support, including system default, ask-each-time and a specific enabled account.
- Calling-account identity and available number/provider information where Android exposes it.
- Calling-from and called-line information kept distinct from the remote caller's number.
- Incoming call UI, call notifications, lock-screen handling and configurable answer gestures.
- Home opening-page selection (Contacts, Recents or last used).
- Assisted dialing and regional number formatting settings.
- Configurable quick responses for incoming calls.
- Flip-to-silence setting where supported.

Google Voice and External-Origin Calls (1.4.9)

- External-origin call screen handling option in phone settings.
- When enabled, Maclean Phone suppresses its own automatic foreground call-screen launch for the applicable outgoing cellular-call path, while retaining Android Telecom call tracking and controls.
- Intended to reduce unwanted UI takeover when an external application, such as Google Voice, initiates a carrier call.
- Existing ordinary SIM calling functionality remains available.
- The option is disabled by default to preserve existing behavior.
- Google Voice retains control of its own account, caller-ID routing and carrier access-number arrangements.
- This feature does not modify Google Voice, change carrier caller ID, or guarantee that Google Voice will display its own in-call interface during a SIM-carried call.

Contacts and Favorites

- Contact browsing, searching, creating, editing and deleting.
- Contact photos and contact details.
- Multiple phone numbers and other contact information.
- Contact grouping and organization.
- Favorites for frequently called contacts.
- VCF/vCard contact import and export.
- Integration with Android contact information where permitted.
- Contact actions from call history.
- Contact-name display in place of raw phone numbers when a matching contact is available.

Integrated CRM

- Contact and customer relationship management.
- CRM-linked contact information.
- Contact notes and organizational details.
- Business-oriented contact records.
- Integration between phone contacts and CRM functions.
- Contact management designed for both personal and business use.

Recent Calls and Call History

- Incoming, outgoing and missed-call history.
- Contact names and telephone numbers.
- Call timestamps and available call details.
- Redial and callback functions.
- Contact creation from recent calls.
- Call-history management.
- Android call-log integration, subject to permissions and platform restrictions.

Calling Accounts and SIM Management

- Use the Android default calling account.
- Ask which SIM or calling account to use.
- Select a preferred physical SIM.
- Display available calling accounts.
- Display account identity information when available.
- Preserve the distinction between outgoing SIM identity and the remote party's number.
- Support Android-managed call routing.

SIP/VoIP Integration

- Integrated SIP/VoIP account configuration.
- Internet-based calling support.
- SIP account registration and status information.
- SIP account management.
- Configurable SIP service settings.
- SIP calling functionality where supported by the configured provider and application components.
- SIP/VoIP audio controls.
- Noise and echo reduction settings for supported VoIP audio paths.

SIP functionality depends on the configured provider, network connectivity, supported codecs and the application's SIP implementation.

Business IVR — Interactive Voice Response

- Automated business telephone directory.
- English and Russian language menu support.
- Configurable IVR directory entries.
- Custom call-routing options.
- Language-based menu selections.
- Business-oriented incoming SIP/VoIP call handling.

Example:

"Press 1 for English."

"Press 2 for Russian."

Callers can then be directed according to the configured IVR directory.

The IVR requires a compatible SIP/VoIP calling arrangement. It does not independently intercept ordinary carrier calls.

Call Forwarding

- Carrier call-forwarding configuration.
- Forward all calls.
- Forward when busy.
- Forward when unanswered.
- Forward when unavailable.
- SIP/VoIP call-forwarding settings where supported.
- Forwarding destination configuration.

Carrier forwarding requires support from the mobile network and may use carrier-specific activation codes.

Voicemail

- Voicemail access.
- Voicemail number configuration.
- Calling-account-related voicemail settings where available.
- Access to carrier-provided voicemail services.

Group Calling and Conferencing

- Android-supported conference calling.
- Group-call management where supported.
- Multiple-call state handling.
- Available call merging and management controls.

Conference availability depends on the carrier, Android telephony implementation and calling account.

Call Recording

- Manual call-recording controls.
- Start Recording and Stop Recording functions.
- Recording status indication.
- Recording storage and access functionality.
- Configurable recording destination where supported.
- Local management of recordings.

Recording is not intended to start automatically without user action.

Important: Android may restrict access to cellular-call audio. Some devices may capture microphone audio only, rather than both sides of a call. Recording availability and quality depend on the device, operating system, audio routing and permissions.

Caller ID and Caller Intelligence

- Incoming caller identification.
- Contact-based caller recognition.
- Local caller information where available.
- Caller announcements.
- Caller-related information displayed during incoming calls.
- Integration with contact records and call history.
- Caller screening and spam-related functionality where supported.

Caller information depends on available local data, Android permissions and supported screening interfaces.

Blocked Numbers and Call Screening

- Blocked-number management.
- Android-supported call-screening integration.
- Caller blocking controls.
- Management of unwanted calls.

Some call-screening functions require Android role assignment or system permissions.

Accessibility

Maclean Phone includes accessibility-oriented settings and controls:

- TalkBack compatibility.
- Text scaling from 100% to 200%.
- Large Controls.
- High Contrast.
- Visual incoming-call alerts.
- Caller announcements.
- Simplified Mode.
- SIP/VoIP noise and echo reduction.
- Hearing-device audio routing where supported.
- Configurable call-answer interaction.

Simplified Mode

Simplified Mode provides larger, easier-to-use controls for:

- Favorites.
- Keypad.
- Recent Calls.
- Voicemail.
- Settings.

Audio and Hearing Support

- Speakerphone controls.
- Microphone muting.
- Available Bluetooth and connected-device audio routes.
- Hearing-device routing where exposed by Android.
- SIP/VoIP noise reduction.
- SIP/VoIP echo reduction.
- Audio route selection during supported calls.

Cellular audio processing is primarily controlled by Android, the modem and the phone manufacturer.

Appearance and Interface Customization

- Light and dark appearance options where available.
- Custom background settings.
- Panel appearance controls.
- Panel opacity adjustment from 1% to 100%.
- Configurable opening page.
- Call-screen appearance and interaction settings.
- Interface adjustments for accessibility and readability.

Notifications

- Incoming-call notifications.
- Missed-call notifications.
- Call-status notifications.
- Notification-related settings.
- Android notification-channel integration where applicable.

Notification behavior depends on Android permissions and system settings.

Security and Privacy

- Android permission-based access to telephone and contact functions.
- Local contact and call-history integration.
- Android-managed cellular call handling.
- Application-specific settings storage.
- Call-screen behavior controls.
- No requirement to replace Android's cellular telephony infrastructure.
- AGPLv3 source licensing.

Important security distinction: Standard SIM-based cellular calls are not end-to-end encrypted by Maclean Phone. Cellular-network encryption, where present, is managed by the carrier and modem.

SIP/VoIP security depends on the configured transport, media-encryption capabilities and provider.

Application Settings

Settings include applicable controls for:

- Calling accounts.
- SIM selection.
- SIP/VoIP configuration.
- Business IVR.
- Call forwarding.
- Voicemail.
- Call recording.
- Contacts and call behavior.
- Caller identification.
- Blocked numbers.
- Accessibility.
- Audio.
- Appearance.
- Notifications.
- External-origin call-screen handling.
- Application information.

Installation

1. Download the latest Maclean Phone APK from GitHub Releases.
2. Allow Android to install applications from the selected source.
3. Open the APK.
4. Select Install.
5. Launch Maclean Phone.
6. Grant the necessary telephone, contacts, microphone, notification and call-related permissions.
7. Set Maclean Phone as the default phone application if you want its full cellular dialer functionality.
8. Configure your preferred SIM, calling account and other settings.

Some features require additional Android permissions or roles.

Updating

Install a newer APK directly over the existing application.

Do not uninstall the previous version first if you want to retain your application data and settings.

To install as an update, the new APK must use:

- The same application ID.
- A compatible signing certificate.
- An appropriate updated version code.

Existing data should be backed up before significant updates.

Technical Information

- Application: Maclean Phone
- Version: 1.4.9
- Version code: 20
- Package: "com.macleanofduartenterprises.phone"
- Platform: Android
- Minimum SDK: 26
- Target SDK: 36
- Compile SDK: 36
- Language: Kotlin/Android
- License: GNU AGPLv3, subject to bundled third-party notices

Important Limitations

Google Voice

Google Voice carrier calling can use a linked cellular SIM while maintaining Google Voice's number routing.

Maclean Phone's external-origin call-screen setting can suppress its own automatic foreground launch, but it cannot force Google Voice to display its proprietary calling interface.

Call Recording

Android and device manufacturers may restrict call-audio capture. Recording both sides of a cellular call is not guaranteed.

SIP/VoIP

SIP features require compatible account configuration, network connectivity and supported provider functionality.

Carrier Call Forwarding

Forwarding depends on the cellular carrier and supported service codes.

Audio Processing

Cellular noise cancellation and echo processing are primarily controlled by Android and device hardware. Application-level audio processing applies to supported VoIP paths.

Hearing Devices

Hearing-device compatibility depends on Android, the device hardware and available audio routes.

Encryption

Maclean Phone does not currently provide independent end-to-end encryption for ordinary SIM-based voice calls.

Version 1.4.9 Highlights

- Added External-origin call screen handling.
- Added configurable suppression of automatic outgoing call-screen foreground launches.
- Improved compatibility behavior for calls initiated by external applications such as Google Voice.
- Preserved Android Telecom call tracking and call management.
- Preserved existing cellular calling functionality.
- Maintained existing calling-account and SIM selection capabilities.
- Updated application version to 1.4.9.
- Updated version code to 20.

Earlier Features and Development

The application has evolved from a standard Android dialer into a combined cellular phone, SIP/VoIP and contact-management application.

Earlier functionality includes:

- Standard cellular calling.
- Multiple SIM selection.
- SIP/VoIP integration.
- Business IVR.
- English and Russian IVR menus.
- Call forwarding.
- Voicemail configuration.
- Manual recording.
- Contacts and Favorites.
- Call history.
- Caller identification.
- Blocked-number management.
- Integrated CRM functionality.
- Accessibility controls.
- Audio routing and processing settings.
- Appearance customization.
- Notification controls.
- Calling-account configuration.

Version 1.2.0 Highlights

- Added Accessibility & Audio settings.
- Added TalkBack support.
- Added text scaling.
- Added Large Controls.
- Added High Contrast.
- Added visual call alerts.
- Added caller announcements.
- Added Simplified Mode.
- Added SIP/VoIP noise and echo reduction.
- Added hearing-device support.
- Added Calling Accounts controls.
- Added SIM selection controls.
- Added SIP/VoIP registration status.
- Expanded panel opacity adjustment to 1%–100%.

Licensing

Maclean Phone is distributed under the GNU Affero General Public License version 3 (AGPLv3), subject to the licensing terms and notices of included third-party components.

See the included license and source files for additional information.

Developer

Maclean Of Duart Enterprises

Android phone application with cellular calling, contacts, CRM and SIP/VoIP integration for home and business use.

Website: https://macleanofduartenterprises.com

Maclean Phone — Version 1.4.9
