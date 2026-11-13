# Release record: Hop v1.1.92 (13 November 2026, Perth)

Made by the hop-ship REC step (Legal123 advice 27 Oct 2026, para 3.7(b)-(d)). Screens drawn from the shipped Hop-Web working tree at commit 79e800f (clean, tag v1.1.92): headless Chromium, 390x844, light theme, network blocked (outside requests answered 204). Script: 1.1.92/build/v1_1_92/tests/rec92.js (from rec91.js; uses prem_lib.js for the Premium screens).

| Item | Value |
|---|---|
| Version | 1.1.92 |
| Reached TestFlight | 13 Nov 2026 14:10 Perth (06:10 UTC), Codemagic iOS build #56 (commit 46fd0fd), 5.1 min, build number 56; upload to App Store Connect succeeded. Codemagic's post-processing added the build to the HP beta group. |
| Reached Google Play | 13 Nov 2026 14:18 Perth (06:18 UTC), Codemagic Android build #53 (commit 5cb47b0), 7.2 min, **version code 53**; the log shows "Uploaded App Bundle ... to Google Play", "Set new release for application com.hoptravel.hop Google Play track alpha" and "Updated release for track alpha". |
| Hop-Web commit | 79e800f (main; index.html and sw.js only, on top of 10 incoming commits 8777237 and earlier: 8 authored as HOPios (visa-overrides, coverage jobs 15 and 16), 1 hop-advisory-bot, 1 hop-entry-recheck-bot; data files and tools/entry-recheck only; Jason approved fast-forwarding, 13 Nov) |
| hop-ios-app commit | 46fd0fd (main; the built commit) |
| Hop_Android commit | 5cb47b0 (main; the built commit) |
| Tags | v1.1.92 on all three repos, on those three commits |
| index.html SHA-256 (web, as committed) | 99ab766c532116979cbc570aa9630353a1a2ea2c2700761f3f1c5af5c5cd8dcd (8,436,086 bytes) |
| www/index.html SHA-256 (the copy inside both apps; identical in hop-ios-app and Hop_Android) | 8a1659a72a959de0acd1bd219fcaff7de5fc8250507d63595305e51ce278fea2 |
| passports.js SHA-256 (unchanged) | 432d240ac111ec0810cd3e366becf3281f572f38688a8aa1818f40a26335d182 |
| images.js SHA-256 (unchanged) | cf95b9b0169cd3ee5cdcdee4d1caebe7be557968bb5305599236607a0070a52f |
| sw.js SHA-256 | 86c71a3cca02f22bb7ed9878952bd5d3ac0bceaeaa71a8f946d5f467332304ee |
| Legal track and version built in | Unchanged from 91: the LEGAL_BUILTIN block in index.html is track 2, applying from 12 November 2026 (measured: "track": 2 and applies_from 2026-11-12 in both the 91 and the 92 build). |
| hop-data | Only this record folder is added by the release (after a fast-forward over one hop-visa-overrides-bot data commit, bc10c26: visa-overrides*.json only). |
| Premium | Prices come from the store (RevenueCat). The Premium screens in this folder use canned test prices (A$34.99 a year, A$4.99 a month) and a stubbed store plug-in: **demo, no payment**. |
| What changed in this release | P10 swipe back from the left half of an iPhone page; P16/P18 the map pop-up's guide looks like the list page's; P17 titles and short blurbs for 634 guide items that had none; P19 thin selected-country outline; exchange rates refreshed to the 12 Nov dataset. No change to the legal text, the Premium code, storage keys or the network address list. |

## What blocks use until the person answers
- First launch (fresh install): index.html, function _lgFirstRun (notice "Before you start"; the rest waits until Continue).
- Changed Terms or Disclaimer: index.html, function _lgGate (the I agree pop-up is _lgPopTerms; the "If you do not agree" screen is _lgDisagree).
- Proof for this release: the first-launch capture was taken on the shipped tree from a fresh browser context and showed only the notice ("Before you start") before any tap (render check printed notice true, title "Before you start", 5 storage keys written by the app at boot). The legal block was measured unchanged from 91 (same track and date); this release did not re-run the legal behaviour suite (legal_t.js).
- The I agree screen is the real built-in text, opened by calling _lgPopTerms directly; legal behaviour is unchanged from 90, whose legal_t.js passed 377 / 377.

## Screens in this folder
first-launch, i-agree, do-not-agree, and the Premium screen for the iPhone and Android looks, each as the top of the screen and the small print below it (**demo, no payment**). 7 PNGs.

## Not covered
- A completed purchase on Android (no signed-in Google account on the test machine); Restore and a real purchase are checked on an iPhone.
- Hop-Web's own privacy.html (9,317 bytes, last changed in v1.1.87) is not the 18,070-byte privacy.html in the 92 web build folder (identical to 90's and 91's). The release changed neither; the website's /privacy page is built from privacy.html (rule 17): the legal chat should check which one is meant to be live. Same note as the 91 record.
