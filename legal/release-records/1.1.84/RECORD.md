# Release record: Hop v1.1.84 (3 November 2026)

Made by the hop-ship REC step (Legal123 advice 27 Oct 2026, para 3.7(b)-(d)). Screens drawn from the shipped Hop-Web working tree at commit 12b9d72: headless Chromium, 390x844, light theme, network blocked.

| Item | Value |
|---|---|
| Version | 1.1.84 |
| Reached TestFlight | 3 Nov 2026, Codemagic iOS build #47 finished 05:53 UTC (13:53 AWST); added to the HP beta group by the App Store Connect task; submitted to TestFlight beta review (state WAITING_FOR_REVIEW when checked) |
| Reached Google Play | 3 Nov 2026, Codemagic Android build #43 finished 05:57 UTC (13:57 AWST); versionCode 43 published to track alpha (Play review state not checked) |
| Hop-Web commit | 12b9d72 (on main) |
| hop-ios-app commit | b97cd7f (on main) |
| Hop_Android commit | 3c1bee8 (on main) |
| Tags | v1.1.84 on all three repos, on those commits |
| index.html SHA-256 (web, as committed) | f079ffa06f8d9062b01dc2992e129269fdcae2dfa77a71899c4cfe6afa97ae40 |
| www/index.html SHA-256 (the copy inside both apps; identical in hop-ios-app and Hop_Android) | 1c93bae93bb8d801b3bbef01278e7a05b259db54d3298e8082213f90feb0006a |
| passports.js SHA-256 (web, as committed) | 266211840c7af01d23f9c77696298f03f7902e40a86600d3cc9c2276832452f8 |
| Legal track and version built in | unchanged from 1.1.83: track 1, version 2 (Privacy Policy version 2 from 28 Oct 2026; Terms and Disclaimer version 1 from 17 Oct 2026) |

## What blocks use until the person answers
- First launch (fresh install): index.html, function _lgFirstRun (notice "Before you start"; the rest waits until Continue).
- Changed Terms or Disclaimer: index.html, function _lgGate.
- Proof: lw1_render.js run on 84 with 83 as the old build: 28 of 28 checks pass (a fresh install shows only the notice until Continue is tapped). This release did not change the legal text or these functions.

## Screens in this folder
first-launch, i-agree (made-up example change), do-not-agree, and the Premium screen for iPhone and Android looks (**demo, no payment**).

## Not covered
Release 84 changed the reader, data, Document Lock, NZ advisory wording and the Data sources and attribution sheet. It did not change any legal text or screen shown above.
