# Release record: Hop v1.1.90 (12 November 2026)

Made by the hop-ship REC step (Legal123 advice 27 Oct 2026, para 3.7(b)-(d)). Screens drawn from the shipped Hop-Web working tree at commit 8d7bfaa (clean, tag v1.1.90): headless Chromium, 390x844, light theme, network blocked (outside requests answered 204). Script: 1.1.90/build/v1_1_90/tests/rec90.js (uses prem_lib.js for the Premium screens).

| Item | Value |
|---|---|
| Version | 1.1.90 |
| Reached TestFlight | 12 Nov 2026, Codemagic iOS build #54 (commit fc8ec0b), 4.8 min, App.ipa 163.5 MB, build number 54; upload to App Store Connect succeeded. Codemagic's post-processing added build 54 to HP and submitted it for Beta App Review; that was corrected by hand the same day (Remove from Review, HP removed from build 54 only). Now: HI group only, status Ready to Submit, no external review. Earlier attempt iOS #53 (commit bbd3f2b) failed in 1.4 min at the RevenueCat key check step, before any upload; its artifacts were never used. |
| Reached Google Play | 12 Nov 2026, Codemagic Android build #51 (commit 179eb95), 5.4 min, app-release.aab 173.4 MB, **version code 51**; "Successfully published App Bundle to Google Play track alpha". Earlier attempt Android #50 (commit 8de2bf9) failed in 0.9 min at the same step, before any upload; it used no version code. |
| Hop-Web commit | 8d7bfaa918eb9b39e6ebd4fa09fd9cf92646a540 (main; index.html and sw.js only). Its commit message quotes an index.html SHA-256 starting a4bd1d8a, which is NOT the file's hash: the committed file hashes to c6cf79b9 (below), matching the iOS and Android commit messages and SHIP-REPORT.md. The message is stale, the file is right. |
| hop-ios-app commit | fc8ec0b235ab8446ff65d1603a87f92e0b6bd683 (main; built commit bbd3f2b plus the check_rc_keys fix) |
| Hop_Android commit | 179eb95529c57e567018670ea6e500dd4bd402a5 (main; built commit 8de2bf9 plus the same fix) |
| Tags | v1.1.90 on all three repos, on those three commits (verified 12 Nov 2026) |
| index.html SHA-256 (web, as committed) | c6cf79b95ba832baf1022bc5c046a179d5add5437a11cc6e4d48b9b3fc2e8b01 (8,291,299 bytes) |
| www/index.html SHA-256 (the copy inside both apps; identical in hop-ios-app and Hop_Android) | aaa04d2b61b665dcce0510c0f8e4c04cfb313a809647b2b2d51c934bdd56178c |
| passports.js SHA-256 (unchanged from 88/89) | 432d240ac111ec0810cd3e366becf3281f572f38688a8aa1818f40a26335d182 |
| images.js SHA-256 | cf95b9b0169cd3ee5cdcdee4d1caebe7be557968bb5305599236607a0070a52f |
| sw.js SHA-256 | d8c7138592df6c529c154165cefb8c508c36cc2cef8c5f43477b95ef85b044d7 |
| Legal track and version built in | **Changed from 89.** The LEGAL_BUILTIN block in index.html is track 2, version 1, published 12 Nov 2026 (Privacy Policy, Terms and Disclaimer each "Version 1, applying from 12 November 2026"; Terms and Disclaimer change "material", Privacy "significant"). 89 had track 1 version 3. |
| hop-data | The built-in legal text is the only copy shipped; the legal data files for the hop-data legal tree and privacy.html were held for 1.2.0 by decision F2, so the live legal feed does not yet carry track 2. Nothing else pushed to hop-data by the build. |
| Premium | New in 90: RevenueCat (plugin 14.1.0), prices from the store. The Premium screens in this folder use canned test prices (A$34.99 a year, A$4.99 a month) and a stubbed store plug-in: **demo, no payment**. |

## What blocks use until the person answers
- First launch (fresh install): index.html, function _lgFirstRun (notice "Before you start"; the rest waits until Continue).
- Changed Terms or Disclaimer: index.html, function _lgGate (the I agree pop-up is _lgPopTerms; the "If you do not agree" screen is _lgDisagree). From 90, _lgGate leaves the Premium status row visible; body.lggate CSS keeps only Manage or cancel subscription for a subscriber, and documents stay open.
- Proof for this release: the first-launch capture was taken on the shipped tree from a fresh browser context and showed only the notice ("Before you start") before any tap (render check printed notice true, title "Before you start", 5 storage keys written by the app at boot). The 90 verifier (verify90.js, VERIFICATION.txt item [9]) proved the data side: the built-in LEGAL_BUILTIN equals track-2.json and the app reads track 2. A full render run of the legal pop-ups was NOT made for 90 (VERIFICATION-G.txt says the legal pop-ups were not tested), so the only render proof for the blocking behaviour in this release is the first-launch capture above plus the three pop-up captures in this folder.
- The I agree screen is the real 1.1.90 built-in text (summaries and date taken from LEGAL_BUILTIN), opened by calling _lgPopTerms directly (the app's own upgrade path to that pop-up was not render-tested in this release). SHIP-REPORT.md's "upgrade 89 to 90 proof" covers saved data kept, not the pop-up.

## Screens in this folder
first-launch, i-agree, do-not-agree, and the Premium screen for the iPhone and Android looks, each as the top of the screen and the small print below it (**demo, no payment**). 7 PNGs.

## Not covered
- Android R8 stays off; the emulator workflow was drafted, never run.
- The wrappers were verified by verify_ios (108/0) and verify_android (137/0), not by a native run of the RevenueCat plug-in; real purchase and Restore are Jason's phone checks (SHIP-REPORT.md).
- Apple App Privacy "Device ID" answer is still open and blocks external TestFlight review.
- The website was not deployed for 90; privacy.html was held for 1.2.0.
