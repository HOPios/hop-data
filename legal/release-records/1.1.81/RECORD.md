# Release record: Hop v1.1.81 (30 October 2026)

Made by the hop-ship REC step (Legal123 advice 27 Oct 2026, para 3.7(b)-(d)). Screens were drawn from the shipped Hop-Web working tree at commit b905513: headless Chromium, 390x844, light theme, network blocked.

| Item | Value |
|---|---|
| Version | 1.1.81 |
| Reached TestFlight | 30 Oct 2026, Codemagic iOS build #44 finished 06:26 UTC; added to the HP beta group by the App Store Connect task |
| Reached Google Play | 30 Oct 2026, Codemagic Android build #40 finished 06:31 UTC; versionCode 40 uploaded and set on track alpha (Play review state not checked) |
| Hop-Web commit | b905513 (on main) |
| hop-ios-app commit | a910438 (on main) |
| Hop_Android commit | 1251ade (on main) |
| index.html SHA-256 (web, as committed) | 6352ae9f4b5f502211c101a782f6e60fb27c774805f1dd7dcd7d4305df52bfbe |
| www/index.html SHA-256 (the copy inside both apps) | 7c4087a3c4d62dc7137def90a54d4667e764c65dece19a784696ea650f5dc0a2 |
| Legal track and version built in | track 1, version 2 (Privacy Policy version 2 applies from 28 Oct 2026; Terms of Service and Disclaimer are version 1, applying from 17 Oct 2026) |

## What blocks use until the person answers
- First launch (fresh install): `index.html`, function `_lgFirstRun` (the notice "Before you start"; the passport sheet and the rest of the app wait behind it until Continue is tapped). It writes agreed_terms, agreed_at and agreed_ts into the saved record hop_legal_seen.
- Changed Terms or Disclaimer: `index.html`, function `_lgGate` (until "I agree", only Settings > Document lock, Settings > Legal and support work).
- Proof: the render test `build\v1_1_81\tests\lw1_render.js` (checks LW1-1, LW1-2, LW1-6, LW1-7: a fresh install shows only the notice and no passport sheet, also after a relaunch before Continue, and the passport sheet follows Continue). 28 of 28 pass; 80 fails LW1-OLD as it must.

## Screens in this folder
- 1.1.81_first-launch_2026-10-30.png : the first-launch notice (new in 81)
- 1.1.81_i-agree_2026-10-30.png : the "I agree" notice (made-up example change; beta short form)
- 1.1.81_do-not-agree_2026-10-30.png : the "If you do not agree" screen (beta form)
- 1.1.81_subscription-ios-demo-no-payment_2026-10-30.png and 1.1.81_subscription-android-demo-no-payment_2026-10-30.png : the Premium screen as it stands. **Demo, no payment**: it unlocks the paid tier locally; real payment is not wired up.
