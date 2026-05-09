# Continuous Improvement Toolbox Privacy Policy

_Effective date: May 9, 2026_
_Contact: CravenAppDevelopment@icloud.com_

---

## What Information We Collect

**Continuous Improvement Toolbox does not collect personal information.**

We do not operate any server that receives data from the app. Continuous Improvement Toolbox has no user accounts, no sign-up, no login, and no analytics, crash reporting, advertising, or telemetry of any kind. We do not collect your name, email address, IP address, device identifier, location, or any other personally identifying information.

## What Is Stored on Your Device

All app data is stored **locally on your device** in a SwiftData (SQLite) database inside the app's Application Support container. No data is stored in iCloud Drive, no Core Data, no Keychain, no shared App Group, and no UserDefaults.

The local database may contain:

- **Settings you enter in the app** — company name, company address, company contact, PDF report footer text, preferred units (metric/imperial), appearance mode, default tags, and other preferences.
- **Projects you create** — name, notes, customer, location, plant, project owner, reference number, tags, and timestamps.
- **Tool sessions you record** — session name, notes, tool type, pass/fail status, duration, tags, and the measurement data produced by the tool (lap times, decibel samples, lux readings, RPM, vibration samples, pitch/roll, distance, line balancing entries, takt time inputs, and Wi-Fi latency samples). For Wi-Fi sessions, the SSID (network name) of the network you measured and the target hostname you measured against are stored alongside the latency results.
- **Exports** — when you export a session, a CSV or PDF file is written to a temporary location on the device and shared via the standard iOS share sheet. iOS clears these temporary files automatically.

This data never leaves your device except as described in the next two sections.

## iCloud Settings Sync (NSUbiquitousKeyValueStore)

A small subset of your **app settings** is synchronized across devices signed into the same Apple ID using Apple's iCloud Key-Value Store. This is a built-in Apple service; the data is transmitted to and stored by Apple, not by us. We have no access to it.

The settings that are synced are:

- Appearance mode and preferred units
- Default tags
- "Include photos in PDF" and "Sound feedback" preferences
- **Company name, company address, company contact, and PDF report footer text** — if you enter these in Settings, the strings are transmitted to Apple's iCloud Key-Value Store and synced to your other devices.

If you do not want this information synced through iCloud, you can sign out of iCloud or disable iCloud Drive for Continuous Improvement Toolbox in your device's Settings app. No project data, session data, or measurement data is ever transmitted via this mechanism — only the settings listed above.

CloudKit is **not** used by this app. Your projects and sessions remain on the device they were created on.

## Network Connections

The app makes one category of outbound network connection, and only when you actively use the **Wi-Fi Signal** tool:

- The Wi-Fi Signal tool opens a brief TCP connection to a target host (default `1.1.1.1`, Cloudflare's public DNS resolver) to measure round-trip latency. You can change the target host to any hostname you choose. Only a TCP handshake is performed — no payload is sent and no payload is received. The connection is closed immediately after the round-trip time is measured.
- Reading the current Wi-Fi network name (SSID) uses a local Apple system API and does not contact any remote server.

The app contains no analytics SDK, crash reporter, advertising SDK, remote configuration service, push notification service, or App Store receipt validation. Apart from the user-initiated Wi-Fi latency measurement above, the app makes no network requests.

## Third-Party Services and SDKs

**None.** Continuous Improvement Toolbox has no Swift Package Manager, CocoaPods, or Carthage dependencies. The app uses only Apple's first-party frameworks (SwiftUI, SwiftData, AVFoundation, CoreMotion, ARKit, Vision, CoreLocation, NetworkExtension, the Network framework, and Swift Charts).

## Sensor Access and Permissions

The app uses several device sensors to perform live measurements. **Sensor data is read in real time and is not recorded as audio, video, or photographs.** When measurements are saved to a session, they are saved as numeric values only.

- **Microphone** (`NSMicrophoneUsageDescription`) — used by the Decibel Meter to compute sound pressure levels. Only numeric dB values are stored; no audio is recorded.
- **Camera** (`NSCameraUsageDescription`) — used by the Light Meter (lux), the Tachometer CV mode, and the Distance tool (ARKit). The camera feed is processed on-device for measurement only; no photos or video are saved.
- **Motion** (`NSMotionUsageDescription`) — used by the Inclinometer (pitch/roll) and Vibration Analyzer (accelerometer). Only numeric measurements are stored.
- **Location** (`NSLocationWhenInUseUsageDescription`) — required by iOS solely so the Wi-Fi Signal tool can read the current network's SSID via the system Wi-Fi API. **Your geographic coordinates are not read, stored, or transmitted by this app.**

The app does not request access to your photo library, contacts, Bluetooth, Face ID, or App Tracking Transparency, and does not register for push notifications.

## Audience and Children's Privacy

Continuous Improvement Toolbox is a professional productivity tool intended for adult users in workplace and educational contexts. It is not directed at children.

We do not knowingly collect personal information from any user, including children under the age of 13 in compliance with the U.S. Children's Online Privacy Protection Act (COPPA), children under the age of 16 in compliance with the EU General Data Protection Regulation (GDPR), or minors under the age of 18 in compliance with the California Consumer Privacy Act (CCPA).

The app is structurally designed to make such collection impossible: there is no account system, no upload mechanism, and no transmission of identifying information to any server we control.

If you believe a minor has somehow provided personal information through Continuous Improvement Toolbox, please contact us at CravenAppDevelopment@icloud.com and we will respond promptly.

## Data Security

Because Continuous Improvement Toolbox stores all data locally on your device, your data is protected by your operating system's built-in device encryption and the security of your Apple ID and iCloud account. We do not operate servers that store your personal data.

## Your Rights

Because we do not collect personal information, there is no personal data for us to delete, correct, or export on your behalf. To remove all data this app has stored, delete the app from your device. To remove the small set of synced settings described in the **iCloud Settings Sync** section, sign out of iCloud or disable iCloud for Continuous Improvement Toolbox in your device's Settings app, then delete the app. Questions about data associated with your iCloud account should be directed to Apple.

For any questions about this Privacy Policy, contact us at **CravenAppDevelopment@icloud.com**.

## Changes to This Policy

We may update this Privacy Policy from time to time. When we make material changes, we will update the effective date above. Continued use of Continuous Improvement Toolbox after any update constitutes acceptance of the revised policy.

---

*Continuous Improvement Toolbox is an independent product developed by Andrew Craven. Continuous Improvement Toolbox is not affiliated with, endorsed by, or sponsored by Apple, or by any standards body, certification organization, or trademark holder associated with Lean, Six Sigma, Kaizen, or any related continuous improvement methodology.*
