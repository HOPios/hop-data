# Release record: Hop v1.1.85 (4 November 2026)

Made by the hop-ship REC step (Legal123 advice 27 Oct 2026, para 3.7(b)-(d)). Screens drawn from the shipped Hop-Web working tree at commit 49c968b: headless Chromium, 390x844, light theme, network blocked (outside requests answered 204).

| Item | Value |
|---|---|
| Version | 1.1.85 |
| Reached TestFlight | 4 Nov 2026, Codemagic iOS build #48 finished 11:31 UTC (19:31 AWST), version code 48; App Store Connect build f3ebb588-77b2-4a22-a02f-fe385b8c1326 finished processing, was added to the HP beta group by the App Store Connect task and submitted to TestFlight beta review (state WAITING_FOR_REVIEW when checked) |
| Reached Google Play | 4 Nov 2026, Codemagic Android build #44 finished 11:38 UTC (19:38 AWST); versionCode 44 uploaded and set as the release on track alpha (Play review state not checked) |
| Hop-Web commit | 49c968b (on main) |
| hop-ios-app commit | 545f596 (on main) |
| Hop_Android commit | 428ab65 (on main) |
| Tags | v1.1.85 on all three repos, on those commits |
| index.html SHA-256 (web, as committed) | be05c17bc210408e0e5d134ec12b9e567af97977e56def8f678c58140124d4b1 |
| www/index.html SHA-256 (the copy inside both apps; identical in hop-ios-app and Hop_Android) | d75e3034be2a947ce7332ddb8fe190e2bdc8660622dd2525b3e1052a3efc6ab8 |
| passports.js SHA-256 (web, as committed) | e2c6423183fb3a08c4f13eea852d17065931039cdd771d9f471147437112cf85 (identical to 1.1.84) |
| Legal track and version built in | unchanged from 1.1.84: track 1, version 2 (Privacy Policy version 2 from 28 Oct 2026; Terms and Disclaimer version 1 from 17 Oct 2026) |

## What blocks use until the person answers
- First launch (fresh install): index.html, function _lgFirstRun (notice "Before you start"; the rest waits until Continue).
- Changed Terms or Disclaimer: index.html, function _lgGate.
- Proof: lw1_render.js run on 85 with 84 as the old build: 28 of 28 checks pass (a fresh install shows only the notice until Continue is tapped). This release did not change the legal text or these functions.

## Screens in this folder
first-launch, i-agree (made-up example change), do-not-agree, and the Premium screen for iPhone and Android looks (**demo, no payment**).

## Not covered
Release 85 changed the photo reader (status bar, dates, per-flight places, booking reference, 12-hour times), the NZ built-in advisory timestamp, the exchange-rate table, the Check and Explore region rows (globes, counts), the enlarged-globe view, the independence notice size and the passport-at-a-glance card. It did not change any legal text or screen shown above.
