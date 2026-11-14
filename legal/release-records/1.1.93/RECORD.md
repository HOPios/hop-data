# Release record: Hop v1.1.93 (14 November 2026, Perth)

Made by the hop-ship REC step (Legal123 advice 27 Oct 2026, para 3.7(b)-(d)). Screens drawn from the shipped Hop-Web working tree at commit 76e2300 (clean, tag v1.1.93): headless Chromium, 390x844, light theme, network blocked (outside requests answered 204). Script: 1.1.93/tests/rec93.js (from rec92.js; uses prem_lib.js for the Premium screens).

| Item | Value |
|---|---|
| Version | 1.1.93 |
| Reached TestFlight | 14 Nov 2026 10:35 Perth (02:35 UTC), Codemagic iOS build #57 (commit 31e741f), 4.5 min, version 1.1.93; upload to App Store Connect succeeded. Codemagic's post-processing added the build to the HP beta group ("Added build '27794fdb-...' to 'HP' beta group"). |
| Reached Google Play | 14 Nov 2026 10:42 Perth (02:42 UTC), Codemagic Android build #54 (commit 4c2d70d), 6.6 min, **version code 54**; the log shows "Uploaded App Bundle ... to Google Play", "Set new release for application com.hoptravel.hop Google Play track alpha" and "Updated release for track alpha". |
| Hop-Web commit | 76e2300 (main; index.html and sw.js only, on top of 9 incoming commits up to d1cb6e4: 5 authored as HOPios (visa-overrides and weekly page check), 1 hop-home-runner, 1 hop-advisory-bot, 1 hop-entry-recheck-bot, 1 earlier bot commit; data files and tools/entry-recheck only; Jason approved fast-forwarding, 14 Nov) |
| hop-ios-app commit | 31e741f (main; the built commit) |
| Hop_Android commit | 4c2d70d (main; the built commit) |
| Tags | v1.1.93 on all three repos, on those three commits |
| index.html SHA-256 (web, as committed) | e4837786012135e89336c7869156a0dd23f835ff8e716cee403dac27ea7efc58 (8,431,535 bytes) |
| www/index.html SHA-256 (the copy inside both apps; identical in hop-ios-app and Hop_Android) | 893322f78b32cf5a6624641b712df5869152de87e0235f588caa8fc6ad3a5679 |
| passports.js SHA-256 (unchanged) | 432d240ac111ec0810cd3e366becf3281f572f38688a8aa1818f40a26335d182 |
| images.js SHA-256 (unchanged) | cf95b9b0169cd3ee5cdcdee4d1caebe7be557968bb5305599236607a0070a52f |
| sw.js SHA-256 | e118e00da3583ce8c47f0e6a5b79a24663224be4d159de7cbd70378dde75fde7 |
| Legal track and version built in | Unchanged from 92: the LEGAL_BUILTIN block in index.html is track 2, version 1, applying from 12 November 2026 (measured in the 93 build). |
| hop-data | Only this record folder is added by the release (after a fast-forward over bot data commits). |
| Premium | Prices come from the store (RevenueCat). The Premium screens in this folder use canned test prices (A$34.99 a year, A$4.99 a month) and a stubbed store plug-in: **demo, no payment**. |
| What changed in this release | Trips guide pop-up looks like the map pop-up and the top strip dims; 47 Practical-tips lines use the 92 title and blurb; Explore list cards and Destination of the day are full-photo cards with a small Save trip chip and the plain capital; long visa notes show as points; changing the passport redraws the Explore list. No change to the legal text, the Premium code, storage keys or the network address list. |

## What blocks use until the person answers
- First launch (fresh install): index.html, function _lgFirstRun (notice "Before you start"; the rest waits until Continue).
- Changed Terms or Disclaimer: index.html, function _lgGate (the I agree pop-up is _lgPopTerms; the "If you do not agree" screen is _lgDisagree).
- Proof for this release: the first-launch capture was taken on the shipped tree from a fresh browser context and showed only the notice ("Before you start") before any tap (render check printed notice true, title "Before you start", 5 storage keys written by the app at boot). The legal block was measured unchanged from 92 (same track and date); this release did not re-run the legal behaviour suite.
- The I agree screen is the real built-in text, opened by calling _lgPopTerms directly.

## Screens in this folder
- 1.1.93_first-launch_2026-11-14.png
- 1.1.93_i-agree_2026-11-14.png
- 1.1.93_do-not-agree_2026-11-14.png
- 1.1.93_subscription-ios-demo-no-payment_2026-11-14.png and ..._small-print_...png
- 1.1.93_subscription-android-demo-no-payment_2026-11-14.png and ..._small-print_...png
