**English** | [Italiano](README.it.md)

<p align="center">
  <img src="MyUnical/Assets.xcassets/AppIcon.appiconset/4-01.png" width="110" alt="MyUnical">
</p>

<h1 align="center">MyUnical</h1>

<p align="center">
  <b>A native iOS companion for students of the University of Calabria (Unical).</b><br>
  Grades, average and credits, exam booking, fees and weekly timetable on top of the university's Esse3 REST API.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/iOS-17%2B-black?logo=apple" alt="iOS 17+">
  <img src="https://img.shields.io/badge/Swift-5-F05138?logo=swift&logoColor=white" alt="Swift 5">
  <img src="https://img.shields.io/badge/UI-SwiftUI-0A84FF" alt="SwiftUI">
  <img src="https://img.shields.io/badge/dependencies-none-success" alt="No dependencies">
  <a href="LICENSE"><img src="https://img.shields.io/badge/license-PolyForm%20Strict%201.0.0-lightgrey" alt="License"></a>
</p>

> [!NOTE]
> Independent, unofficial project, not affiliated with the University of Calabria. The screenshots below contain no
> personal data.

<p align="center">
  <img src="docs/screenshots/login.png" width="230" alt="Sign-in">
  <img src="docs/screenshots/simulatore.png" width="230" alt="Grade simulator">
</p>

## Features

- **Sign-in with university credentials**, stored only in the iOS Keychain.
- **Dashboard** with weighted average, graduation base score, earned and missing credits (CFU) and latest grades.
- **Grade simulator**: how a future grade and its credits change the average.
- **Transcript (Libretto)** with search, and **exam booking** with date, place, time, committee chair, participants
  and notes.
- **Fees**: payment status, invoices with payment code, amounts and dates, payment by QR code with instructions
  for each method.
- **Weekly timetable**: lessons per day with overlap detection, live "now" filter, custom lessons with colours.
- **Offline first**: data cached as JSON and shown without a connection; silent refresh at launch when online.
- **Localised** in Italian, English and Spanish.

## Architecture

- **SwiftUI**, no third-party dependencies.
- **`NetworkManager`**: Esse3 REST client (authentication, career, grades, averages, exam sessions, bookings,
  invoices) with `async`/`await`.
- **`KeychainHelper`** for credentials, **`DataPersistence`** for the JSON cache, **`NetworkMonitor`** for the
  offline state.
- Models in `Models/`, screens in `Views/`.

The Python prototype used to explore the Esse3 API before building the app is in
[unical-esse3-client](https://github.com/mattmeligeni/unical-esse3-client).

## Build

Open `MyUnical.xcodeproj` with Xcode 15 or later and run on a simulator or device (iOS 17+). A Unical account is
required to sign in.

## License

Source-available under the [PolyForm Strict License 1.0.0](LICENSE): you may read the code and run it for
non-commercial purposes; you may not modify, redistribute or publish it without written permission. The name and
the icon are reserved.

---

<sub>© 2024-2026 [Mattia Meligeni](https://mattiameligeni.com) · Not affiliated with the University of Calabria.</sub>
