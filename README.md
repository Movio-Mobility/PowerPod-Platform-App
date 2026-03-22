# PowerPod Platform (B2B)

<p align="center">
  <img src="assets/icons/applogo.png" alt="PowerPod Platform — use the official Tools logo" width="120" />
</p>

**PowerPod Platform** is the B2B companion app for **GridX** operators and integration partners. It connects you to GridX **PowerPod** battery systems so you can monitor telemetry, work with Bluetooth (BLE) data, and use **Platform Tools** (faults, live tags, cell-level insight, and related operator workflows) while you bring up your electric two-wheeler (2W) product.

This repository is intended for teams who have purchased GridX batteries **for development and integration** of their e2W platforms—not for end-consumer swap or retail flows.

---

## Who this is for

If you are **building or validating** an electric 2W around GridX PowerPod hardware, this app helps you:

- See **real-time and cloud (ThingsBoard)** telemetry alongside **BLE** when you are near the pack.
- Use **Platform Tools** oriented screens for diagnostics, tag reference, and deeper pack visibility during bring-up and field tests.
- Stay aligned with GridX **Pulse / BMS / vehicle** telemetry conventions as you integrate motors, controllers, and vehicle CAN where applicable.

---

## Branding: please use the official Tools logo

When you document your integration, share screenshots, or present your work to stakeholders, **use the official PowerPod Platform / Platform Tools logo and GridX-approved assets**—including the app mark above (`assets/icons/applogo.png` in this repo). That keeps partner communications consistent and clearly associates your build with the GridX ecosystem.

---

## Tech stack (high level)

| Area | Notes |
|------|--------|
| **Client** | Flutter (Dart SDK `>=3.4.0 <4.0.0`) |
| **Backend & identity** | Firebase (Auth, Firestore, Messaging, Storage, etc.) |
| **Telemetry** | ThingsBoard (`thingsboard_client`), plus BLE via `flutter_blue_plus` |
| **Maps & device** | Google Maps, geolocation, permissions, local storage (e.g. `sqflite`, `shared_preferences`) |

Cloud Functions and related Node tooling live alongside this app where configured (`firebase-functions`, `firebase-admin` in the project root).

---

## Prerequisites

- [Flutter](https://docs.flutter.dev/get-started/install) installed and on your `PATH`
- A supported **Android** / **iOS** toolchain for your target devices (BLE is core to many flows)
- Access to the **Firebase** project and credentials GridX provides for your partner build (not committed to this repo)

---

## Getting started

From the project root:

```bash
flutter pub get
flutter run
```

For release builds, follow [Flutter’s deployment guides](https://docs.flutter.dev/deployment) for Android and iOS, and use the signing keys and Firebase configuration supplied for your program.

---

## Thank you

Thank you for choosing GridX hardware for your electric 2W development work and for **trusting GridXenergy** as part of your stack. We are glad to power your integration journey and look forward to safe, reliable energy on the road.

---

Designed and Developed in-house @ GridXenergy
