# Release record: Hop v1.1.82 (1 November 2026)

Made by the hop-ship REC step (Legal123 advice 27 Oct 2026, para 3.7(b)-(d)). Screens drawn from the shipped Hop-Web working tree at commit a10eddd: headless Chromium, 390x844, light theme, network blocked.

| Item | Value |
|---|---|
| Version | 1.1.82 |
| Reached TestFlight | 1 Nov 2026, Codemagic iOS build #45 finished 04:10 UTC; added to the HP beta group by the App Store Connect task |
| Reached Google Play | 1 Nov 2026, Codemagic Android build #41 finished 04:14 UTC; versionCode 41 published to track alpha (Play review state not checked) |
| Hop-Web commit | a10eddd (on main; rebased onto four data-only bot commits) |
| hop-ios-app commit | 151f347 (on main) |
| Hop_Android commit | 1d5d21f (on main) |
| index.html SHA-256 (web, as committed) | bf6849e6aed2ee9dc840e92502f8b499784fbbe0698e93f3be93a41f0b18bc21 |
| www/index.html SHA-256 (the copy inside both apps) | d53680454b043cc6f8f421d3b6a567244fa806c62bf87a0d5244cc1fb7ba57e2 |
| Legal track and version built in | unchanged from 1.1.81: track 1, version 2 (Privacy Policy version 2 from 28 Oct 2026; Terms and Disclaimer version 1 from 17 Oct 2026) |

## What blocks use until the person answers
- First launch (fresh install): index.html, function _lgFirstRun (notice "Before you start"; the rest waits until Continue).
- Changed Terms or Disclaimer: index.html, function _lgGate.
- Proof: build\v1_1_82 re-ran 81's lw1_render.js on 82: 28 of 28 pass (a fresh install shows only the notice until Continue is tapped). This release did not change the legal text or these functions.

## Screens in this folder
first-launch, i-agree (made-up example change), do-not-agree, and the Premium screen for iPhone and Android looks (**demo, no payment**).
