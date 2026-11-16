# Release record: Hop v1.1.94 (16 November 2026, Perth)

Made by the hop-ship REC step (Legal123 advice 27 Oct 2026, para 3.7(b)-(d)). Screens drawn from the shipped Hop-Web working tree at commit 6dc08fd (clean, tag v1.1.94): headless Chromium, 390x844, light theme, network blocked (outside requests answered 204). Script: 1.1.94/ship/rec94.js (from rec93.js; uses prem_lib.js for the Premium screens).

| Item | Value |
|---|---|
| Version | 1.1.94 |
| Reached TestFlight | 16 Nov 2026 12:20 Perth (04:20 UTC), Codemagic iOS build #58 (commit 87e4d0f), 4.8 min, version 1.1.94; "UPLOAD SUCCEEDED with no errors". Codemagic's post-processing added the build to the HP beta group ("Added build '307bcffc-...' to 'HP' beta group"). |
| Reached Google Play | 16 Nov 2026 12:25 Perth (04:25 UTC), Codemagic Android build #55 (commit 17a9299), 4.8 min, **version code 55**; the log shows "Uploaded App Bundle ... to Google Play", "Set new release for application com.hoptravel.hop Google Play track alpha", "Updated release for track alpha" and "Successfully published App Bundle to Google Play track alpha". |
| Hop-Web commit | 6dc08fd (main; index.html, sw.js, passports.js, runners/hop-check.js and the visa-overrides writers, on top of 72 incoming commits up to 01b505e: 42 authored as HOPios, 23 as "Hop visa window", 7 by the advisory, entry-recheck, home-runner and visa-watch bots; data files, tools/entry-recheck JSON and one self-test script only; Jason approved fast-forwarding, 16 Nov) |
| hop-ios-app commit | 87e4d0f (main; the built commit) |
| Hop_Android commit | 17a9299 (main; the built commit) |
| hop-data commit | e458acb (visa-overrides-v94.json, empty, and baked/v1.1.94.json) |
| Tags | v1.1.94 on Hop-Web, hop-ios-app and Hop_Android, on those three commits |
| index.html SHA-256 (web, as committed) | e5b7b3fd843c0c7296f1a8ca883ccdeefcac148c97df35080eeb55ea46c801d1 (8,894,174 bytes) |
| www/index.html SHA-256 (the copy inside both apps; identical in hop-ios-app and Hop_Android) | f170729829e233358bd0d736b0973067baa92e6d85cf7bd1152d4aa4f3d40d51 |
| passports.js SHA-256 | 3d6d54ab0c782d4a6a2fd80fa5a839cbb5b22ac1cbc930672bd28202616dc3a6 |
| images.js SHA-256 (unchanged) | cf95b9b0169cd3ee5cdcdee4d1caebe7be557968bb5305599236607a0070a52f |
| sw.js SHA-256 | 4e7e079a6b023ef592f5976e2dbfd231c9e718975e881d78c6b3184b17030378 |
| Legal track and version built in | Unchanged from 93: the LEGAL_BUILTIN block in index.html is track 2, version 1, applying from 12 November 2026 (not changed by this release). |
| hop-data | This record folder, plus the two v94 files above (add-only). |
| Premium | Prices come from the store (RevenueCat). The Premium screens in this folder use canned test prices (A$34.99 a year, A$4.99 a month) and a stubbed store plug-in: **demo, no payment**. |
| What changed in this release | Entry rules show two check dates per card (Visa type and Stay length); the red advisory line is gone from every note; 108 visa cards lose a baked check date; the live visa file is baked into the app and 94 reads visa-overrides-v94.json; the Explore, Destination of the day and every other photo carries one light layer; 44 non-attractions leave Top attractions; the map pop-up shows the plain capital; long names step down on small phones; one Settings sentence added. No change to the legal text or the Premium code. Status override: Jason shipped after CMP with the verifier at 142 of 145 (3 explained fails). |

## What blocks use until the person answers
- First launch (fresh install): index.html, function _lgFirstRun (notice "Before you start"; the rest waits until Continue).
- Changed Terms or Disclaimer: index.html, function _lgGate (the I agree pop-up is _lgPopTerms; the "If you do not agree" screen is _lgDisagree).
- Proof for this release: the first-launch capture was taken on the shipped tree from a fresh browser context and showed only the notice ("Before you start") before any tap (render check printed notice true, title "Before you start", 5 storage keys written by the app at boot). The legal block is unchanged from 93; this release did not re-run the legal behaviour suite.
- The I agree screen is the real built-in text, opened by calling _lgPopTerms directly.

## Screens in this folder
- 1.1.94_first-launch_2026-11-16.png
- 1.1.94_i-agree_2026-11-16.png
- 1.1.94_do-not-agree_2026-11-16.png
- 1.1.94_subscription-ios-demo-no-payment_2026-11-16.png and ..._small-print_...png
- 1.1.94_subscription-android-demo-no-payment_2026-11-16.png and ..._small-print_...png
