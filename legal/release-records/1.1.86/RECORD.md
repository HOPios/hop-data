# Release record: Hop v1.1.86 (5 November 2026)

Made by the hop-ship REC step (Legal123 advice 27 Oct 2026, para 3.7(b)-(d)). Screens drawn from the shipped Hop-Web working tree at commit 1a3ca81: headless Chromium, 390x844, light theme, network blocked (outside requests answered 204).

| Item | Value |
|---|---|
| Version | 1.1.86 |
| Reached TestFlight | 5 Nov 2026, Codemagic iOS build #49 finished 12:23 UTC (20:23 AWST); the App Store Connect upload reported "UPLOAD SUCCEEDED with no errors"; App Store Connect build 6713237e-3847-4fb8-b259-5a8c459a9241 was found after processing and was added to the HP beta group by the App Store Connect task ("Added build ... to 'HP' beta group"). TestFlight build number: 49 (the Codemagic build index; 85's build 48 was Codemagic #48; this run's own log did not print the number) |
| Reached Google Play | 5 Nov 2026, Codemagic Android build #45 finished 12:29 UTC (20:29 AWST); "Successfully published App Bundle to Google Play track alpha"; version code 45 (Play review state not checked) |
| Hop-Web commit | 1a3ca81 (on main; rebased onto the bot data commits up to fa70fec, which Jason approved) |
| hop-ios-app commit | 3668fbd (on main) |
| Hop_Android commit | 2c0d491 (on main) |
| Tags | v1.1.86 on all three repos, on those commits |
| index.html SHA-256 (web, as committed) | 3b89db44b9fb13e2e0936805319202c71af5778f4aaa8c5260e2ed7ae80c058a |
| www/index.html SHA-256 (the copy inside both apps; identical in hop-ios-app and Hop_Android) | 0fff226bd83ec6b9290fa829b4eeb65d050d99084b3cc721c2549ed700881092 |
| passports.js SHA-256 (web, as committed) | 6de9505db2a6332f6d0f81706ff4e6955218039fbc764c5c413562f57252187c |
| Legal track and version built in | unchanged from 1.1.85: track 1, version 2 (Privacy Policy version 2 from 28 Oct 2026; Terms and Disclaimer version 1 from 17 Oct 2026). The legal constants and the first-launch functions are byte-identical to 85 (fingerprint of index.html: 1550 of 1561 top-level segments unchanged, none of them legal). |

## What blocks use until the person answers
- First launch (fresh install): index.html, function _lgFirstRun (notice "Before you start"; the rest waits until Continue).
- Changed Terms or Disclaimer: index.html, function _lgGate.
- Proof for this release: the first-launch capture below was taken on the shipped tree from empty storage and showed only the notice ("Before you start") before any tap. 85's full lw1_render.js run (28 of 28) was NOT re-run for 86; the legal text and these two functions are unchanged from 85.

## Screens in this folder
first-launch, i-agree (made-up example change), do-not-agree, and the Premium screen for iPhone and Android looks (**demo, no payment**).

## Not covered
Release 86 changed: the Check glance card placement after switching Premium on and off, the red cross in the Explore search box when only a Topic is picked and its size (25 px) in every search box, the Explore notice, "Destination of the day" and the heading globe size, the Check drop-downs' widths, seven built-in advisory levels and 446 advisory dates, eight built-in visa values (Cambodia, Saint Vincent and the Grenadines, Singapore, Turkmenistan), the Taiwan note for Canadians, the exchange-rate table, and make_www.js (the Android Tesseract guard). None of these change what a person agrees to. The hop-data texts file for the live "Data sources" text was prepared but NOT published. Real-device behaviour was not tested by this record.
