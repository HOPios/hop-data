# Release record: Hop v1.1.89 (9 November 2026)

Made by the hop-ship REC step (Legal123 advice 27 Oct 2026, para 3.7(b)-(d)). Screens drawn from the shipped Hop-Web working tree at commit 7419b95: headless Chromium, 390x844, light theme, network blocked (outside requests answered 204). Script: 1.1.89\build\v1_1_89\tests\rec89.js.

| Item | Value |
|---|---|
| Version | 1.1.89 |
| Reached TestFlight | 9 Nov 2026, Codemagic iOS build #52 finished 07:35 UTC (15:35 AWST); the App Store Connect upload reported "UPLOAD SUCCEEDED with no errors"; App Store Connect build 451990f2-2eec-4dc6-b8ff-3e6c7561abf1 was added to the HP beta group by the App Store Connect task ("Added build ... to 'HP' beta group"). Build number 52. HI group not checked (needs Jason's Apple sign-in). |
| Reached Google Play | 9 Nov 2026, Codemagic Android build #49 finished 08:44 UTC (16:44 AWST); "Uploaded App Bundle ... to Google Play" and "Updated release for track alpha"; version code 49; the .aab is 170,773,497 bytes. Play Console (Test and release > Latest releases and bundles) lists Closed testing - Alpha, version 49, "In review", 178 of 178 countries/regions, bundle uploaded 9 Nov 2026 8:43 AM and Active. Size for new installs not read this time. An earlier Android attempt, build #48 on the same commit, failed in 2.5 s before any upload: Gradle's own download of gradle-8.14.3-all.zip from GitHub returned HTTP 504; it used no version code. |
| Hop-Web commit | 7419b95 (on main, on top of the 10 data-only bot commits that were already on origin; only index.html and sw.js changed) |
| hop-ios-app commit | 2a915b6 (on main). storage_origin.json was modified in the working tree and NOT committed. |
| Hop_Android commit | 72edb7d (on main) |
| Tags | v1.1.89 on all three repos, on those commits (no tag existed before) |
| index.html SHA-256 (web, as committed) | f9d6c7ebef798fd8a89d3ab3b95ba80d95145a57e7210e191f23a1a8ec21e429 |
| www/index.html SHA-256 (the copy inside both apps; identical in hop-ios-app and Hop_Android) | 411b2dde609da43da541ab0e4ca11f95610db7ca091149f2821f88c5b11fafa5 |
| passports.js SHA-256 (unchanged from 88) | 432d240ac111ec0810cd3e366becf3281f572f38688a8aa1818f40a26335d182 |
| Legal track and version built in | Unchanged from 88: the LEGAL_BUILTIN block in index.html is byte-identical to 88's (track 1, version 3: Privacy Policy version 3 from 6 Nov 2026; Terms and Disclaimer from 17 Oct 2026). No legal text changed in 89. |
| hop-data | Nothing pushed for 89 by the build: the app still reads visa-overrides-v88.json (VIS skipped by decision). |

## What blocks use until the person answers
- First launch (fresh install): index.html, function _lgFirstRun (notice "Before you start"; the rest waits until Continue).
- Changed Terms or Disclaimer: index.html, function _lgGate.
- Proof for this release: the first-launch capture was taken on the shipped tree from empty storage and showed only the notice ("Before you start") before any tap (render check printed notice true, title "Before you start"). The full legal render run was not re-run for 89; 89 changes neither function.

## Screens in this folder
first-launch, i-agree (made-up example change), do-not-agree, and the Premium screen for the iPhone and Android looks (**demo, no payment**).

## Not covered
Release 89 changes text sizes, Home's Check and Travel history bubbles, trip dates, the Check region rows, buttons' font family and some colours. The advisory refresh (ADV) and visa bake (VIS) were skipped: the advisory gates failed (Canada 230 and New Zealand 222 records outside their bands), so the built-in advisory levels are the same as 88's. The CMP review was done by Jason in the project chat. R8 stays off.
