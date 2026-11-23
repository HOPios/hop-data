# Release record: Hop v1.2.4 (23 November 2026, Perth)

Made by the hop-ship REC step (Legal123 advice 27 Oct 2026, para 3.7(b)-(d)). Screens drawn from the shipped Hop-Web working tree at commit cf0bc45 (tag v1.2.4; index.html SHA-256 0f778c02...fd): headless Chromium, 390x844, light theme, network blocked (outside requests answered 204).

| Item | Value |
|---|---|
| Version | 1.2.4 |
| Reached TestFlight | 23 Nov 2026 10:49 Perth (02:49 UTC), Codemagic iOS build #63 (commit 0472a4f), built with Xcode 27.2 in about 6 min; "UPLOAD SUCCEEDED with no errors". Codemagic's HP step then FAILED (it did not find the build while Apple was still processing; Apple's "finished processing" email came at 11:08 Perth). The build appeared with group HI only; HP was added by hand in App Store Connect on 23 Nov (build 63 now shows HI and HP; Beta App Review "Waiting for Review"). |
| App Store review | Submitted by a project chat with Automatic release; "Waiting for Review" since 11:13 Perth, 23 Nov 2026 (as told by Jason; not read from App Store Connect by this step beyond the app list showing "iOS 1.2.4 Waiting for Review"). |
| Reached Google Play | 23 Nov 2026 10:55 Perth (02:55 UTC), Codemagic Android build #60 (commit 2c538f2), queued about 6 min, built 5 min, **version code 60**; "Successfully published App Bundle to Google Play track alpha". A project chat then sent Production 60 and Alpha for review with managed publishing on (as told by Jason). |
| Hop-Web commit | cf0bc45 (main; index.html and sw.js changed; images.js, passports.js, privacy.html unchanged). Forty-seven commits were fast-forwarded in first with Jason's approval: 40 by Jason (JOB 92 visa work), 5 hop-entry-recheck-bot, 3 hop-advisory-bot, 1 hop-visa-watch-bot (tools/, data and one workflow file; none of the shipped files). |
| hop-ios-app commit | 0472a4f (main; MARKETING_VERSION 1.2.4, xcode pinned to 27.2, ios-sim-smoke workflow, www from the 1.2.4 build) |
| Hop_Android commit | 2c538f2 (main; versionName 1.2.4, www from the 1.2.4 build) |
| Tags | v1.2.4 on Hop-Web cf0bc45, hop-ios-app 0472a4f and Hop_Android 2c538f2 (none existed) |
| index.html SHA-256 (web, as committed) | 0f778c02026b6d6afcb615b456554f431252aca567df5a142fecc0279646a8fd (8,984,753 bytes) |
| www/index.html SHA-256 (inside both apps, as committed; identical in hop-ios-app and Hop_Android) | 3779c8890a382c8c0dfff707737dfe8ba9218804abc0daf0291d981616f3f8fa (8,984,913 bytes) |
| sw.js SHA-256 | 78515bbb7942ddc7edd4121254d2ff1d4995edfc09e105697749e32cc84b6efc |
| privacy.html SHA-256 | 9fe7bfc4c9c44f2be262ac61daded72feafe6eb66710e2bdbc9ddd29d5b03894 (unchanged) |
| passports.js / images.js SHA-256 (unchanged) | 3d6d54ab0c782d4a6a2fd80fa5a839cbb5b22ac1cbc930672bd28202616dc3a6 / cf95b9b0169cd3ee5cdcdee4d1caebe7be557968bb5305599236607a0070a52f |
| Legal track and version built in | Unchanged from 1.2.3: track 2, version 4 (privacy "Version 4, applying from 20 November 2026"). hop-data legal/track-2.json SHA-256 2fea38e83b06083f99dc358d658b4c3ffb943185ae6cabc28ec9a6162bb74dc0 (not touched by this release). |
| Website | Not deployed (no website change in 1.2.4). |
| Premium | Prices come from the store (RevenueCat). The Premium screens in this folder use canned test prices (A$34.99 a year, A$4.99 a month) and a stubbed store plug-in: **no payment**. |
| What changed in this release | Hop no longer shows travel advice outside the Travel advisory section: the red advice banner under "Worth the detour" is gone, and advice sentences are removed from guide text (Best time to visit and a Yemen line), the Yemen destination text and, if an old value returns, visa fields. The L1-L4 advisory badge and the Travel advisory section are unchanged. iPhone builds now use Xcode 27.2 (the iOS 27 SDK). No change to Terms, Disclaimer or Privacy, no new network address, no change to what is collected. |

## What blocks use until the person answers
- First launch (fresh install): index.html, function _lgFirstRun (notice "Before you start"; the rest waits until Continue).
- Changed Terms or Disclaimer: index.html, function _lgGate (the I agree pop-up is _lgPopTerms; the "If you do not agree" screen is _lgDisagree).
- Proof for this release: the first-launch capture was taken on the shipped tree from a fresh browser context and showed only the notice before any tap (render check printed notice true, title "Before you start", 5 storage keys written by the page).
- No legal text changed in 1.2.4, so no new notice is shown on upgrade (no "upgrade-no-popup" capture this release). The I agree screen is the built-in layout opened by calling _lgPopTerms directly with the built-in summary (not a real notice).

## Screens in this folder
1.2.4_first-launch, 1.2.4_i-agree, 1.2.4_do-not-agree and 1.2.4_subscription-{ios,android}-demo-no-payment (top and -small-print), all _2026-11-23.png.
