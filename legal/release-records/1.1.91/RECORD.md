# Release record: Hop v1.1.91 (13 November 2026, Perth)

Made by the hop-ship REC step (Legal123 advice 27 Oct 2026, para 3.7(b)-(d)). Screens drawn from the shipped Hop-Web working tree at commit 32a7cdb (clean, tag v1.1.91): headless Chromium, 390x844, light theme, network blocked (outside requests answered 204). Script: 1.1.91/build/v1_1_91/tests/rec91.js (from rec90.js; uses prem_lib.js for the Premium screens).

| Item | Value |
|---|---|
| Version | 1.1.91 |
| Reached TestFlight | 13 Nov 2026 07:28 Perth (12 Nov 23:28 UTC), Codemagic iOS build #55 (commit b3726f1), 5.1 min, App.ipa 163.6 MB, build number 55; upload to App Store Connect succeeded. Codemagic's post-processing added build 55 to HP and submitted it for Beta App Review (allowed for 91: Apple App Privacy now lists Device ID). |
| Reached Google Play | 13 Nov 2026 07:33 Perth (12 Nov 23:33 UTC), Codemagic Android build #52 (commit 468e7b8), 5.0 min, app-release.aab 170.7 MB, **version code 52**; "Successfully published App Bundle to Google Play track alpha". |
| Hop-Web commit | 32a7cdb93a9d93d992a9e924b5a222f1e77e1e84 (main; index.html and sw.js only, on top of 7 data-only visa-overrides commits 04c0231..2a01500 that Jason approved fast-forwarding, 13 Nov) |
| hop-ios-app commit | b3726f13a93a438d1ad35575d9f382275be8f567 (main; the built commit) |
| Hop_Android commit | 468e7b8829a1937133b6d2a8533535624c6bd900 (main; the built commit) |
| Tags | v1.1.91 on all three repos, on those three commits |
| index.html SHA-256 (web, as committed) | 82183181f691a9442220ddfeed7c3e9b8dcf24d4dc493d111bfb2da3b2d63e45 (8,303,024 bytes) |
| www/index.html SHA-256 (the copy inside both apps; identical in hop-ios-app and Hop_Android) | cd5ae08506df8ca8db45e6b9aee654401903384670cd95630110fee19210be58 |
| passports.js SHA-256 (unchanged from 88/89/90) | 432d240ac111ec0810cd3e366becf3281f572f38688a8aa1818f40a26335d182 |
| images.js SHA-256 | cf95b9b0169cd3ee5cdcdee4d1caebe7be557968bb5305599236607a0070a52f |
| sw.js SHA-256 | 79f20e28bbbb6134c8afcdff5ad0630d371be4d55f4cd8e39244341914e4bdf6 |
| Legal track and version built in | Unchanged from 90: the LEGAL_BUILTIN block in index.html is track 2, version 1, applying from 12 November 2026 (measured: "track": 2 in both the 90 base and the 91 build). |
| hop-data | Only this record folder is added by the release. |
| Premium | Prices come from the store (RevenueCat). The Premium screens in this folder use canned test prices (A$34.99 a year, A$4.99 a month) and a stubbed store plug-in: **demo, no payment**. |
| Android shrinking | R8 is ON from this release (minifyEnabled true, optimize rules, no shrinkResources). AAB BUNDLE-METADATA: r8.json says obfuscation, optimization and shrinking enabled; the share of code NOT affected is 22.85 % / 23.53 % / 23.03 %; mapping file proguard.map (42,612,636 bytes) is in the AAB. Proof: build\v1_1_91\notes\r8\final_build23\ (46 checks x 4 runs, all PASS). |

## What blocks use until the person answers
- First launch (fresh install): index.html, function _lgFirstRun (notice "Before you start"; the rest waits until Continue).
- Changed Terms or Disclaimer: index.html, function _lgGate (the I agree pop-up is _lgPopTerms; the "If you do not agree" screen is _lgDisagree).
- Proof for this release: the first-launch capture was taken on the shipped tree from a fresh browser context and showed only the notice ("Before you start") before any tap (render check printed notice true, title "Before you start", 5 storage keys written by the app at boot). The legal block was measured unchanged from 90 (track 2 in both); this release did not re-run the legal behaviour suite (legal_t.js).
- The I agree screen is the real built-in text, opened by calling _lgPopTerms directly (the app's own upgrade path to that pop-up was not render-tested in this release; legal behaviour is unchanged from 90, whose legal_t.js passed 377 / 377).

## Screens in this folder
first-launch, i-agree, do-not-agree, and the Premium screen for the iPhone and Android looks, each as the top of the screen and the small print below it (**demo, no payment**). 7 PNGs.

## Not covered
- A completed purchase on Android (the emulator has no signed-in Google account); Restore and a real purchase are checked on an iPhone.
- The photo reader's language file was missing from every Android build before this one (measured on the Play AABs of 1.1.87 to 1.1.90: entry present only without ".gz"); 91 is the first build where the guard proves the file is in the bundle.
- Hop-Web's own privacy.html (9,317 bytes) is not the 18,070-byte privacy.html in the 91 web build folder (identical to 90's). The release did not change either; the website's /privacy page is built from privacy.html (rule 17): the legal chat should check which one is meant to be live.
