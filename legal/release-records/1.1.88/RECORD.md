# Release record: Hop v1.1.88 (8 November 2026)

Made by the hop-ship REC step (Legal123 advice 27 Oct 2026, para 3.7(b)-(d)). Screens drawn from the shipped Hop-Web working tree at commit a1f332c: headless Chromium, 390x844, light theme, network blocked (outside requests answered 204).

| Item | Value |
|---|---|
| Version | 1.1.88 |
| Reached TestFlight | 8 Nov 2026, Codemagic iOS build #51 finished 03:28 UTC (11:28 AWST); the App Store Connect upload reported "UPLOAD SUCCEEDED with no errors"; App Store Connect build 177b56fb-027c-461a-9b21-b62b11d97ab5 was found after processing and added to the HP beta group by the App Store Connect task ("Added build ... to 'HP' beta group"). Build number 51. The .ipa is 157,060,355 bytes. The HI group was NOT read: App Store Connect needs Jason's Apple sign-in; HP is from the Codemagic log. |
| Reached Google Play | 8 Nov 2026, Codemagic Android build #47 finished 03:33 UTC (11:33 AWST); "Successfully published App Bundle to Google Play track alpha"; version code 47. Play Console lists 47.aab (1.1.88) as Active, size for new installs 167 MB (under the 175 MB stop line), time to download 1m 31s; the .aab is 170,770,811 bytes. The Alpha release itself showed "In review" (178 countries / regions); 1.1.87 stayed "Available to selected testers". |
| Hop-Web commit | a1f332c9fff698012a1408c7e9853012d075b87b (on main; includes the v88 overrides writers and runners/hop-check.js) |
| hop-ios-app commit | 4a08b6f50847806a3e4c8c4500d7695cec456ba5 (on main) |
| Hop_Android commit | c68c6fde031d8209168d5d9516978465713260d0 (on main) |
| hop-data | main a6dca5bda63cde3d19d0f48240192d83e1a66778: visa-overrides-v88.json (empty, schema 1) and baked/v1.1.88.json (the 290 entries baked into 88), pushed before the repos |
| Tags | v1.1.88 on all three repos, on those commits |
| index.html SHA-256 (web, as committed) | e0c02d4010ff37b60548f0aa24a5d87297b46c5be00b60d89166875c400bc1b3 |
| www/index.html SHA-256 (the copy inside both apps; identical in hop-ios-app and Hop_Android) | 5de02c993400b051518f57838d9087f87bb52f10c11dd7f9fe23da9ca726354b |
| passports.js SHA-256 (web, as committed) | 432d240ac111ec0810cd3e366becf3281f572f38688a8aa1818f40a26335d182 |
| Legal track and version built in | track 1, version 3 (published 6 Nov 2026): Privacy Policy version 3 from 6 Nov 2026; Terms and Disclaimer from 17 Oct 2026. Unchanged since 87; no legal text changed in 88. |

## What blocks use until the person answers
- First launch (fresh install): index.html, function _lgFirstRun (notice "Before you start"; the rest waits until Continue).
- Changed Terms or Disclaimer: index.html, function _lgGate.
- Proof for this release: the first-launch capture was taken on the shipped tree from empty storage and showed only the notice ("Before you start") before any tap. The full legal render run (lw1_render.js) was not re-run for 88; 88 changes neither function.

## Screens in this folder
first-launch, i-agree (made-up example change), do-not-agree, and the Premium screen for iPhone and Android looks (**demo, no payment**). The Premium screen now shows the new globe-and-star badge and the Check icon on "Full visa detail" (88).

## Not covered
Release 88 adds the Home tab (restyled to the spec's measurements), the tab bar change on every tab, the new Premium badge, the "Best on Wi-Fi" photo line, the "No visas to arrange" Trips wording, the Android Auto-fill "PDF works best" line, the 8 capital wordings, the Saint Martin credit author, the Burundi DE advisory level, and the v88 overrides file and background-check change. R8 stays off (the emulator could not run on Codemagic). Verified with headless Chromium and WebKit; real phones are checked on TestFlight and Play Alpha after this release.
