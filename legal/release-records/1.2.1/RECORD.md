# Release record: Hop v1.2.1 (19 November 2026, Perth)

Made by the hop-ship REC step (Legal123 advice 27 Oct 2026, para 3.7(b)-(d)). Screens drawn from the shipped Hop-Web working tree at commit d487a5e (tag v1.2.1): headless Chromium, 390x844, light theme, network blocked (outside requests answered 204).

| Item | Value |
|---|---|
| Version | 1.2.1 |
| Reached TestFlight | 19 Nov 2026 16:48 Perth (08:48 UTC), Codemagic iOS build #60 (commit a7a0771), queued 1 min, built 6 min, version 1.2.1; "UPLOAD SUCCEEDED with no errors, 1 warning". Post-processing: "Added build '1fd3cf7e-6232-412f-8801-1ca46f47bad9' to 'HP' beta group". Not submitted to App Store review. |
| Reached Google Play | 19 Nov 2026 16:55 Perth (08:55 UTC), Codemagic Android build #57 (commit f8a3ff0), queued 7 min, built 6 min, **version code 57**; "Successfully published App Bundle to Google Play track alpha". Not promoted to Production. |
| Hop-Web commit | d487a5e (main; index.html and sw.js changed; images.js, passports.js, privacy.html and runners/hop-check.js byte-identical to 1.2.0), on top of 15 incoming commits up to ded5aa4 (8 bot commits, 7 by Jason's own HOPios identity; Jason approved the fast-forward) |
| hop-ios-app commit | a7a0771 (main; MARKETING_VERSION 1.2.1, www from the 1.2.1 build) |
| Hop_Android commit | f8a3ff0 (main; versionName 1.2.1, www, Capacitor Android 8.5.0 -> 8.6.2, scripts/emu_net.js) |
| Tags | v1.2.1 on Hop-Web d487a5e, hop-ios-app a7a0771 and Hop_Android f8a3ff0 (none existed) |
| index.html SHA-256 (web, as committed) | 5ebc598143e421437d0693b602b73a626c3a511386e0221b7c237582414b374a (8,940,074 bytes) |
| www/index.html SHA-256 (inside both apps; identical in hop-ios-app and Hop_Android) | 17849bf3b60d9f4518c726c82626e082c79ae490e268c9a3eff6ec6cbec541de |
| sw.js SHA-256 | a49dba8639f90a96b8bebdb0bf60bfa2038b582fd4f8874f39fc4165700edb85 |
| passports.js / images.js / privacy.html SHA-256 (unchanged from 1.2.0) | 3d6d54ab0c782d4a6a2fd80fa5a839cbb5b22ac1cbc930672bd28202616dc3a6 / cf95b9b0169cd3ee5cdcdee4d1caebe7be557968bb5305599236607a0070a52f / eeafed09ddf7dbe9ee96b229d1ffc7abc966a92dfdeb8049ed5a67b584923935 |
| Legal track and version built in | LEGAL_BUILTIN in index.html: track 2, version 2 (applying from 17 November 2026). Unchanged from 1.2.0: the legal text, the gate and the privacy text were not touched in this release. |
| Premium | Prices come from the store (RevenueCat). The Premium screens in this folder use canned test prices ($34.99 a year, $4.99 a month) and a stubbed store plug-in: **no payment**. |
| What changed in this release | The top bar's shadow lost its 9999px page-colour spread (light: 0 1px 4px at 6% stays; dark: none, as 1.2.0). Version strings 1.2.1 in the seven places. Android: Capacitor 8.5.0 -> 8.6.2. No change to text, data, legal or privacy. |

## What blocks use until the person answers
- First launch (fresh install): index.html, function _lgFirstRun (notice "Before you start"; the rest waits until Continue).
- Changed Terms or Disclaimer: index.html, function _lgGate (the I agree pop-up is _lgPopTerms; the "If you do not agree" screen is _lgDisagree).
- Proof for this release: the first-launch capture was taken on the shipped tree from a fresh browser context and showed only the notice before any tap (render check printed notice true, title "Before you start", 5 storage keys written by the page).
- The I agree screen is the built-in layout opened by calling _lgPopTerms directly with an example summary dated 19 Nov 2026 (not a real notice).

## Screens in this folder
1.2.1_first-launch, 1.2.1_i-agree, 1.2.1_do-not-agree, and 1.2.1_subscription-{ios,android}-demo-no-payment (top and -small-print), all _2026-11-19.png.
Not in this release: privacy-ok-notice (no privacy change).
