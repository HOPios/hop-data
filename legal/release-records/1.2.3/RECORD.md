# Release record: Hop v1.2.3 (20 November 2026, Perth)

Made by the hop-ship REC step (Legal123 advice 27 Oct 2026, para 3.7(b)-(d)). Screens drawn from the shipped Hop-Web working tree at commit 6af9b7b (tag v1.2.3): headless Chromium, 390x844, light theme, network blocked (outside requests answered 204).

| Item | Value |
|---|---|
| Version | 1.2.3 |
| Reached TestFlight | 20 Nov 2026 18:44 Perth (10:44 UTC), Codemagic iOS build #62 (commit f932d8f), built in about 6 min, version 1.2.3; "UPLOAD SUCCEEDED with no errors, 1 warning" (the warning: built with the iOS 26.5 SDK; from April 2027 Apple requires the iOS 27 SDK). Post-processing: "Added build '65ef80a1-01ef-459c-a755-9aa61def7cd5' to 'HP' beta group". |
| Reached Google Play | 20 Nov 2026 18:50 Perth (10:50 UTC), Codemagic Android build #59 (commit 5ca7786), queued 6 min, built 5 min, **version code 59**; "Updated release for track alpha". Not promoted to Production. |
| Hop-Web commit | 6af9b7b (main; index.html, sw.js and privacy.html changed; images.js and passports.js unchanged). Four data-only commits (advisory bot, entry-recheck bot, two by Jason) were fast-forwarded in first; nothing of mine was rebased. |
| hop-ios-app commit | f932d8f (main; MARKETING_VERSION 1.2.3, www from the 1.2.3 build) |
| Hop_Android commit | 5ca7786 (main; versionName 1.2.3, www from the 1.2.3 build) |
| Tags | v1.2.3 on Hop-Web 6af9b7b, hop-ios-app f932d8f and Hop_Android 5ca7786 (none existed) |
| index.html SHA-256 (web, as committed) | ef680f5f964488309fb236ee1c826ab0192ba07c74cdf97d30e0b17ec4be280c (8,951,435 bytes). This is the verified build 88f0a1c0f509ae5b3635b9de951d435c85dc583b153dde8e8a1aed0b4b54c74c with the ship date filled in (3 places). |
| www/index.html SHA-256 (inside both apps; identical in hop-ios-app and Hop_Android) | 58e05c2af0bdc853e9d9627191eb86084445f3f17ad4735a1e144b61d9fd0bdf (8,951,595 bytes) |
| sw.js SHA-256 | a82add2b57761864be2e54a4f7ca6d038788d7279a11b3b655bfa7eae8232bdc |
| privacy.html SHA-256 | 9fe7bfc4c9c44f2be262ac61daded72feafe6eb66710e2bdbc9ddd29d5b03894 |
| passports.js / images.js SHA-256 (unchanged from 1.2.2) | 3d6d54ab0c782d4a6a2fd80fa5a839cbb5b22ac1cbc930672bd28202616dc3a6 / cf95b9b0169cd3ee5cdcdee4d1caebe7be557968bb5305599236607a0070a52f |
| Legal track and version built in | LEGAL_BUILTIN in index.html: track 2, version 4 (privacy "Version 4, applying from 20 November 2026", minor; Terms and Disclaimer minor, text unchanged). Published live to hop-data legal/track-2.json (commit bca19e7, SHA-256 2fea38e83b06083f99dc358d658b4c3ffb943185ae6cabc28ec9a6162bb74dc0; GitHub raw and jsDelivr both serve it). |
| Website | LIVE-B6 deployed 20 Nov 2026 (privacy Version 4 on /privacy; 246 of 246 served files hash-identical to the zip; only privacy, terms and earlier-versions changed). |
| Premium | Prices come from the store (RevenueCat). The Premium screens in this folder use canned test prices (A$34.99 a year, A$4.99 a month) and a stubbed store plug-in: **no payment**. |
| What changed in this release | Hop's anonymous usage counts cover more: a place opened from the Check tab or as the destination of the day, an official link tapped (and which kind), a trip created or a stop added, whether Auto-fill worked, a Redeem code tap, a place marked as visited, whether Hop was opened offline, and a failed download. The same body as before (passport code, app version, iPhone or Android, plus at most one extra value); never search text, trips, documents or any ID. The switch in Settings > Legal stops all of it. Privacy Policy Version 4 says so (flag minor: no pop-up). |

## What blocks use until the person answers
- First launch (fresh install): index.html, function _lgFirstRun (notice "Before you start"; the rest waits until Continue).
- Changed Terms or Disclaimer: index.html, function _lgGate (the I agree pop-up is _lgPopTerms; the "If you do not agree" screen is _lgDisagree).
- Privacy change: this release's change is minor, so no notice is shown (the capture 1.2.3_upgrade-no-popup shows Check right after an upgrade from 1.2.2 storage; the render check found no overlay).
- Proof for this release: the first-launch capture was taken on the shipped tree from a fresh browser context and showed only the notice before any tap (render check printed notice true, title "Before you start", 5 storage keys written by the page).
- The I agree screen is the built-in layout opened by calling _lgPopTerms directly with an example summary (not a real notice). In 1.2.3 Terms and Disclaimer text did not change.

## Screens in this folder
1.2.3_first-launch, 1.2.3_i-agree, 1.2.3_do-not-agree, 1.2.3_upgrade-no-popup, and 1.2.3_subscription-{ios,android}-demo-no-payment (top and -small-print), all _2026-11-20.png.
