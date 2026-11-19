# Release record: Hop v1.2.2 (19 November 2026, Perth)

Made by the hop-ship REC step (Legal123 advice 27 Oct 2026, para 3.7(b)-(d)). Screens drawn from the shipped Hop-Web working tree at commit 2c78a1d (tag v1.2.2): headless Chromium, 390x844, light theme, network blocked (outside requests answered 204).

| Item | Value |
|---|---|
| Version | 1.2.2 |
| Reached TestFlight | 19 Nov 2026 18:45 Perth (10:45 UTC), Codemagic iOS build #61 (commit 7286afc), queued 4 min, built 5 min, version 1.2.2; "UPLOAD SUCCEEDED with no errors, 1 warning" (the warning: built with the iOS 26.5 SDK; from April 2027 Apple requires the iOS 27 SDK). Post-processing: "Added build 'ccda43e7-7e52-438b-a68a-5e9f98bb4e08' to 'HP' beta group". Not submitted to App Store review. |
| Reached Google Play | 19 Nov 2026 18:58 Perth (10:58 UTC), Codemagic Android build #58 (commit 16e1532), queued 15 min, built 7 min, **version code 58**; "Updated release for track alpha". Not promoted to Production. |
| Hop-Web commit | 2c78a1d (main; index.html, sw.js and privacy.html changed; images.js and passports.js unchanged), nothing incoming from bots at push time |
| hop-ios-app commit | 7286afc (main; MARKETING_VERSION 1.2.2, www from the 1.2.2 build) |
| Hop_Android commit | 16e1532 (main; versionName 1.2.2, www from the 1.2.2 build) |
| Tags | v1.2.2 on Hop-Web 2c78a1d, hop-ios-app 7286afc and Hop_Android 16e1532 (none existed) |
| index.html SHA-256 (web, as committed) | 4798e201649dfff4383ee4554a178f256a4554abc07de74d36793827b878b13a (8,946,940 bytes) |
| www/index.html SHA-256 (inside both apps; identical in hop-ios-app and Hop_Android) | 2b8e296e6b5d32ff9d7c51f3fb651ec5b98c78bd159f981971e7991d7fa3a820 (8,947,100 bytes) |
| sw.js SHA-256 | a340bcf6e6970757da74611da97dd0790f194ec1fb3cfcd50a7a8765d97c8693 |
| privacy.html SHA-256 | abdc6102ae89dc4969676479e4b33fbe742c6614ff236e1ae3a66ab84c556b8f |
| passports.js / images.js SHA-256 (unchanged from 1.2.1) | 3d6d54ab0c782d4a6a2fd80fa5a839cbb5b22ac1cbc930672bd28202616dc3a6 / cf95b9b0169cd3ee5cdcdee4d1caebe7be557968bb5305599236607a0070a52f |
| Legal track and version built in | LEGAL_BUILTIN in index.html: track 2, version 3 (privacy "Version 3, applying from 19 November 2026", significant; Terms and Disclaimer minor, text unchanged). Published live to hop-data legal/track-2.json (commit b7de1f9, SHA-256 66354f0b1c88168b7548e5ea82ccfd4eb10ae3b1bbee04504c92d4039452f68b) and archived as t2-v3-2026-11-19.json. |
| Website | LIVE-B5 deployed 19 Nov 2026 (privacy Version 3 on /privacy; 246 of 246 served files hash-identical to the zip). |
| Premium | Prices come from the store (RevenueCat). The Premium screens in this folder use canned test prices (A$34.99 a year, A$4.99 a month) and a stubbed store plug-in: **no payment**. |
| What changed in this release | Hop now counts, anonymously, which parts of the app are used (nine events to Hop's own counter at count.hoptravelapp.com, run on Cloudflare; passport code, app version, iPhone or Android, day and country only; never search text, trips, documents or any ID). A switch in Settings, under Legal ("Share anonymous usage counts"), turns it off. Privacy text Version 3. Version strings 1.2.2 in the seven places. |

## What blocks use until the person answers
- First launch (fresh install): index.html, function _lgFirstRun (notice "Before you start"; the rest waits until Continue).
- Changed Terms or Disclaimer: index.html, function _lgGate (the I agree pop-up is _lgPopTerms; the "If you do not agree" screen is _lgDisagree).
- Privacy change: a significant privacy change shows the "We've updated our Privacy Policy" notice (OK / Read what changed); it does not block use.
- Proof for this release: the first-launch capture was taken on the shipped tree from a fresh browser context and showed only the notice before any tap (render check printed notice true, title "Before you start", 5 storage keys written by the page).
- The I agree screen is the built-in layout opened by calling _lgPopTerms directly with an example summary (not a real notice). In 1.2.2 Terms and Disclaimer text did not change, so no I agree pop-up is shown to people.

## Screens in this folder
1.2.2_first-launch, 1.2.2_i-agree, 1.2.2_do-not-agree, 1.2.2_privacy-ok-notice (the new privacy change notice, with the 1.2.2 summary), and 1.2.2_subscription-{ios,android}-demo-no-payment (top and -small-print), all _2026-11-19.png.
