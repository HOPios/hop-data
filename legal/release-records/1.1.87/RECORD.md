# Release record: Hop v1.1.87 (6 November 2026)

Made by the hop-ship REC step (Legal123 advice 27 Oct 2026, para 3.7(b)-(d)). Screens drawn from the shipped Hop-Web working tree at commit aacd8bd: headless Chromium, 390x844, light theme, network blocked (outside requests answered 204).

| Item | Value |
|---|---|
| Version | 1.1.87 |
| Reached TestFlight | 6 Nov 2026, Codemagic iOS build #50 finished 12:06 UTC (20:06 AWST); the App Store Connect upload reported "UPLOAD SUCCEEDED with no errors"; App Store Connect build 758d777d-da61-419e-83aa-81b4600919bb was found after processing and added to the HP beta group by the App Store Connect task ("Added build ... to 'HP' beta group"). Build number 50. The .ipa is 157,067,122 bytes; App Store Connect's own download size was not read (sign-in is Jason's). |
| Reached Google Play | 6 Nov 2026, Codemagic Android build #46 finished 12:13 UTC (20:13 AWST); "Successfully published App Bundle to Google Play track alpha"; version code 46. Play Console lists 46.aab (1.1.87) as Active, size for new installs 167 MB; the .aab is 170,777,593 bytes. The release itself showed "In review" on the app dashboard. |
| Hop-Web commit | aacd8bd (on main; includes the merge of vo87-writers, e5897ef) |
| hop-ios-app commit | 8b8fb56 (on main) |
| Hop_Android commit | 85e9100 (on main) |
| hop-data | main 6d08387: texts/track-1.json v2, visa-overrides-v87.json (empty), baked/v1.1.87.json, legal/track-1.json version 3 with legal/archive/t1-v3-2026-11-06.json and the CHANGELOG row (legal v2 archive was already there, identical) |
| Tags | v1.1.87 on all three repos, on those commits |
| index.html SHA-256 (web, as committed) | 6c4eea1c11ee54412571e23d5f803a4a23e35e8c9e77981aa63783695cb5f706 |
| www/index.html SHA-256 (the copy inside both apps; identical in hop-ios-app and Hop_Android) | aa82012fbc8c6a3c9af1a752944fe50d81f7295a0d82c8aeac72bf1d647e9641 |
| passports.js SHA-256 (web, as committed) | f695640b7600f68807336c79ddfc9c3f0245de3a90c96f7a0e95d6f5acb965ea |
| Legal track and version built in | track 1, version 3. Privacy Policy version 3 from 6 Nov 2026 (adds the paragraphs on photo requests to Cloudflare and Premium photos saved on the phone; change "minor", so no pop-up); Terms and Disclaimer version 1 from 17 Oct 2026, unchanged. |

## What blocks use until the person answers
- First launch (fresh install): index.html, function _lgFirstRun (notice "Before you start"; the rest waits until Continue).
- Changed Terms or Disclaimer: index.html, function _lgGate.
- Proof for this release: the first-launch capture was taken on the shipped tree from empty storage and showed only the notice ("Before you start") before any tap. The full legal render run (lw1_render.js) was not re-run for 87; the 87 changes to these two functions are none (the legal constants changed: privacy text v3 and its allow-list entry).

## Screens in this folder
first-launch, i-agree (made-up example change), do-not-agree, and the Premium screen for iPhone and Android looks (**demo, no payment**).

## Not covered
Release 87 changed Premium photos (516 Premium photos now come from Cloudflare R2 and can be saved on the phone), the Explore cards (slim "Add to trip" chip), the Capital / Currency facts card, the saving-progress chip, the privacy text, and the built-in visa data baking. Stage G (R8) moved to 88. Verified with headless Chromium and WebKit; real phones are checked on TestFlight and Play Alpha after this release.
