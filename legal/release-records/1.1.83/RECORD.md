# Release record: Hop v1.1.83 (2 November 2026)

Made by the hop-ship REC step (Legal123 advice 27 Oct 2026, para 3.7(b)-(d)). Screens drawn from the shipped Hop-Web working tree at commit 21e4e36: headless Chromium, 390x844, light theme, network blocked.

| Item | Value |
|---|---|
| Version | 1.1.83 |
| Reached TestFlight | 2 Nov 2026, Codemagic iOS build #46 finished 20:31 UTC on 1 Nov (04:31 AWST on 2 Nov); added to the HP beta group by the App Store Connect task |
| Reached Google Play | 2 Nov 2026 AWST, Codemagic Android build #42 finished 20:37 UTC on 1 Nov; versionCode 42 published to track alpha (Play review state not checked) |
| Hop-Web commit | 21e4e36 (on main) |
| hop-ios-app commit | 6649b3a (on main) |
| Hop_Android commit | f13cb33 (on main) |
| Tags | v1.1.83 on all three repos, on those commits |
| index.html SHA-256 (web, as committed) | 130fc992522ad933a8e35a1f4481c7eaa5d5a3a0e4876ec9824e393fba7da91a |
| www/index.html SHA-256 (the copy inside both apps; identical in hop-ios-app and Hop_Android) | 6d27af717f7806b45fb7de27c6008edd0850898b5862266543a5720d62c5ed06 |
| Legal track and version built in | unchanged from 1.1.82: track 1, version 2 (Privacy Policy version 2 from 28 Oct 2026; Terms and Disclaimer version 1 from 17 Oct 2026) |

## What blocks use until the person answers
- First launch (fresh install): index.html, function _lgFirstRun (notice "Before you start"; the rest waits until Continue).
- Changed Terms or Disclaimer: index.html, function _lgGate.
- Proof: 81's lw1_render.js run on 83: 27 of 28 checks pass (a fresh install shows only the notice until Continue is tapped; it fits at 320 and 390, light and dark, both looks). The one FAIL is that test's own "LW1-OLD" check, which expects the old build handed to it to be 80 (no notice); it was given 82 here and fails the same way with 82 as the new build. This release did not change the legal text or these functions.

## Screens in this folder
first-launch, i-agree (made-up example change), do-not-agree, and the Premium screen for iPhone and Android looks (**demo, no payment**).

## Not covered
Release 83 changed Auto-fill and pop-up positions; it did not change any legal text or screen shown above.
