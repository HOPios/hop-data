# Release record: Hop v1.2.0 (16 November 2026, Perth)

Made by the hop-ship REC step (Legal123 advice 27 Oct 2026, para 3.7(b)-(d)). Screens drawn from the shipped Hop-Web working tree at commit a8e2f40 (tag v1.2.0): headless Chromium, 390x844, light theme, network blocked (outside requests answered 204).

| Item | Value |
|---|---|
| Version | 1.2.0 (the launch build) |
| Reached TestFlight | 16 Nov 2026 17:39 Perth (09:39 UTC), Codemagic iOS build #59 (commit ebb68fb), 6 min, version 1.2.0; "UPLOAD SUCCEEDED with no errors". Post-processing: "Added build '0c3d3055-ec2d-48b6-8c98-1262d368fb64' to 'HP' beta group" (TestFlight Beta App Review for that group: WAITING_FOR_REVIEW). Not submitted to App Store review. |
| Reached Google Play | 16 Nov 2026 17:45 Perth (09:45 UTC), Codemagic Android build #56 (commit 4d748e6), 6 min, **version code 56**; "Successfully published App Bundle to Google Play track alpha". Not promoted to Production. |
| Hop-Web commit | a8e2f40 (main; index.html, sw.js, privacy.html, runners/hop-check.js, images.js and passports.js unchanged, plus the visa-overrides v120 writers and the texts validator fix, on top of 21 incoming commits up to 68015eb: 18 by Jason's own identities (HOPios, Jason Hop) and 3 entry-recheck bot commits; Jason approved the fast-forward) |
| hop-ios-app commit | ebb68fb (main; the built commit) |
| Hop_Android commit | 4d748e6 (main; the built commit) |
| hop-data commits | 4bcac10 (legal/track-2.json version 2, archive t2-v1-2026-11-17 and t2-v2-2026-11-17, CHANGELOG, texts/track-1.json version 3) and 9be67e5 (baked/v1.2.0.json, visa-overrides-v120.json with 17 entries) |
| Tags | v1.2.0 on Hop-Web, hop-ios-app and Hop_Android, on those three commits |
| index.html SHA-256 (web, as committed) | 97456a6440197803df0306311afc8f0f70e9ad356d69c1e1d095d543a67c1936 (8,940,111 bytes) |
| www/index.html SHA-256 (the copy inside both apps; identical in hop-ios-app and Hop_Android) | 272b0bbc9f3cffbf7115141ed0372de9e06be3c77d3be429a47ab1b0115c9b38 |
| passports.js SHA-256 | 3d6d54ab0c782d4a6a2fd80fa5a839cbb5b22ac1cbc930672bd28202616dc3a6 |
| images.js SHA-256 (unchanged) | cf95b9b0169cd3ee5cdcdee4d1caebe7be557968bb5305599236607a0070a52f |
| sw.js SHA-256 | df39ca81f735d11bc4a262087efaa0276c0a867a011948a3525d1ade8629479d |
| Legal track and version built in | LEGAL_BUILTIN in index.html is track 2, version 2, applying from 17 November 2026 (privacy significant, Terms and Disclaimer minor). Published at hop-data legal/track-2.json the same day. |
| Premium | Prices come from the store (RevenueCat). The Premium screens in this folder use canned test prices (A$34.99 a year, A$4.99 a month) and a stubbed store plug-in: **no payment**. The new "Store:" line shows the currency and price because the stub has no storefront. |
| What changed in this release | Premium screen "Store: country, currency, price" line; Privacy Policy Purchases bullet (RevenueCat also receives your app store's country and basic phone details), shown once as an OK notice to people on track 2 version 1; Settings visa-check paragraph; Turkmenistan fits at the largest text; stronger shadow on the capital line; iPhone and Android portrait only; advisory dates refreshed (Canada baked); visa baseline = 94 plus the live file at the freeze, app reads visa-overrides-v120.json. |

## What blocks use until the person answers
- First launch (fresh install): index.html, function _lgFirstRun (notice "Before you start"; the rest waits until Continue).
- Changed Terms or Disclaimer: index.html, function _lgGate (the I agree pop-up is _lgPopTerms; the "If you do not agree" screen is _lgDisagree).
- Changed Privacy Policy (significant): the OK notice "We've updated our Privacy Policy" (1.2.0_privacy-ok-notice), opened by the real gate for a person whose saved state is track 2 privacy version 1.
- Proof for this release: the first-launch capture was taken on the shipped tree from a fresh browser context and showed only the notice ("Before you start") before any tap (render check printed notice true, title "Before you start", 5 storage keys written by the page).
- The I agree screen is the real built-in text, opened by calling _lgPopTerms directly.
