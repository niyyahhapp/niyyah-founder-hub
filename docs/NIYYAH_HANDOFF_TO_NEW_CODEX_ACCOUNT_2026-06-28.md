# NIYYAH Handoff To New Codex Account

Updated: June 28, 2026

Use this file as the first message/context for a new Codex account. It summarizes the current NIYYAH project state, what matters, what is risky, and where the important files live.

## One-Line Product

NIYYAH is a calm Qur'an understanding and reflection app that helps Muslim youth and young adults understand the Qur'an one ayah at a time.

## Core Product Rules

- Do not redesign from scratch.
- Keep the experience calm, gentle, beginner-friendly, and low cognitive load.
- Arabic Qur'an text must never be generated, rewritten, or altered.
- Translation and tafsir must show their source.
- Source tafsir should be collapsed by default.
- Beginner explanations and surah notes are educational drafts until reviewed by a qualified Islamic reviewer.
- If there is no verified historical context or reason for revelation, hide that section instead of filling it with generic text.
- Do not present NIYYAH as a scholar, fatwa service, therapist, or religious authority.
- Do not add paid feature/paywall language right now. Monetization is paused until later.

## Public Links

- Public app repo: https://github.com/niyyahhapp/niyyah-app
- Public app preview: https://niyyahhapp.github.io/niyyah-app/app/
- Waitlist repo: https://github.com/niyyahhapp/niyyah-waitlist
- Waitlist page: https://niyyahhapp.github.io/niyyah-waitlist/

## Current Local Source Of Truth

Main web app package:

```text
outputs/NIYYAH-app-public-github-pages/
```

Important public app files:

```text
outputs/NIYYAH-app-public-github-pages/index.html
outputs/NIYYAH-app-public-github-pages/app/index.html
outputs/NIYYAH-app-public-github-pages/app/quran-data.js
outputs/NIYYAH-app-public-github-pages/app/surahs.json
outputs/NIYYAH-app-public-github-pages/auth/index.html
outputs/NIYYAH-app-public-github-pages/auth/auth-config.js
outputs/NIYYAH-app-public-github-pages/privacy.html
outputs/NIYYAH-app-public-github-pages/terms.html
```

Upload-only package:

```text
outputs/UPLOAD_THIS_PUBLIC_APP_ONLY/
```

Private founder hub:

```text
outputs/NIYYAH-private-hub-github-pages/
```

Native SwiftUI project:

```text
outputs/Nia/Nia.xcodeproj
outputs/Nia/Nia/
```

App Store screenshot drafts:

```text
outputs/NIYYAH-app-store-assets/
```

## Current Data Scope

- Al-Fatihah.
- Juz 28, Juz 29, and Juz 30.
- 58 surahs.
- 1,139 ayahs.
- Local data file: `outputs/NIYYAH-app-public-github-pages/app/quran-data.js`.

The app currently loads:

- Arabic ayah text.
- Saheeh International translation via Quran.com API label.
- Ibn Kathir abridged/source tafsir labels where imported.
- Reflection prompts.
- Surah and ayah metadata.

## Current Web App Features

Implemented in the browser app preview:

- First-download onboarding.
- Returning-user daily entry.
- Home screen.
- Surah picker grouped by Al-Fatihah, Juz 28, Juz 29, Juz 30.
- Ayah reading screen.
- Understand section.
- Source tafsir accordion.
- Reflection journal.
- Journal list.
- Progress screen.
- Favorites.
- Vocabulary explainer and vocabulary bank.
- Quizzes.
- Learning journeys.
- NIYYAH Circles local preview.
- Local profile preview.
- Memorization status.
- Blank-page protection if `quran-data.js` fails to load.

## Current Native iOS Status

There is a SwiftUI project in `outputs/Nia/`, but it is behind the browser prototype.

Static checks passed:

- `Info.plist` is valid.
- `project.pbxproj` is valid.
- `Resources/ayahs.json` parses.
- `Resources/surahs.json` parses.

Cannot complete here yet:

- Real Xcode build.
- iPhone Simulator test.
- TestFlight upload.
- App Store archive.

Reason: this Mac/Codex environment currently points to Apple Command Line Tools, not full Xcode. `xcodebuild` reports that full Xcode is required.

## Current Auth Status

Google login UI exists in:

```text
outputs/NIYYAH-app-public-github-pages/auth/
```

Supabase config file:

```text
outputs/NIYYAH-app-public-github-pages/auth/auth-config.js
```

Current visible config includes a Supabase URL and publishable key. Actual login still depends on:

- Supabase Google provider enabled.
- Google OAuth client ID/secret configured.
- GitHub Pages URL added to Supabase redirect URLs.
- Google authorized origins/redirect URI configured correctly.

Do not claim login works until tested on the live GitHub Pages URL.

## Current Stripe / Payment Status

Payment/monetization is paused for now.

Public app currently should not show live paid feature language or public checkout links.

Stripe test links exist only in a private setup doc:

```text
outputs/NIYYAH-private-hub-github-pages/docs/NIYYAH_STRIPE_PAYMENT_LINKS_SETUP.md
```

Those are test links and should not be published publicly.

Important App Store rule risk:

- Do not put Stripe checkout buttons inside the iOS app for digital features.
- Use Apple In-App Purchase / StoreKit later for paid digital app features if needed.
- Website support/donation links can be handled separately after final review.

## Legal / App Store Materials

Drafts exist:

```text
outputs/NIYYAH_APP_STORE_LISTING_DRAFT.md
outputs/NIYYAH_PRIVACY_POLICY_DRAFT.md
outputs/NIYYAH_TERMS_OF_USE_DRAFT.md
outputs/NIYYAH_TESTFLIGHT_AND_LEGAL_CHECKLIST.md
outputs/NIYYAH-app-public-github-pages/privacy.html
outputs/NIYYAH-app-public-github-pages/terms.html
```

These need final review before App Store submission, especially:

- Official support email.
- Account deletion policy if login is launched.
- Data practices once Supabase login is active.
- Religious content disclaimer.
- App Privacy answers in App Store Connect.

## App Store Screenshots

Draft screenshots exist:

```text
outputs/NIYYAH-app-store-assets/iphone-6-9-1320x2868/
outputs/NIYYAH-app-store-assets/ipad-12-9-2048x2732/
```

There are 6 iPhone drafts and 6 iPad drafts. They should be reviewed visually before upload.

## Known Risks

- Browser prototype has more features than the native SwiftUI app.
- Native iOS build has not been verified with full Xcode.
- Religious beginner content is draft pending scholarly review.
- Not all surahs have verified historical context or reason for revelation.
- Google login may not work until Supabase/Google OAuth settings are fully tested.
- Payments are not live and should remain off public pages for now.
- Public GitHub upload is manual unless GitHub connector/local git access is available.

## Latest Local Checks

Recent local checks showed:

- Public app `app/index.html` script parses.
- `quran-data.js` loads locally with 1,139 ayahs and 58 surahs.
- Blank-page fallback exists.
- `entry-choice` is active by default so visitors should not see a blank page while scripts load.
- Public app package avoids live Stripe checkout links.
- Upload package homepage was synced with public app homepage.

## Next Best Steps

1. Upload the current public app files to GitHub:

```text
outputs/NIYYAH-app-public-github-pages/index.html
outputs/NIYYAH-app-public-github-pages/app/index.html
outputs/NIYYAH-app-public-github-pages/app/quran-data.js
```

2. Test the live app:

```text
https://niyyahhapp.github.io/niyyah-app/app/
```

3. Finish and test Supabase Google login on the live URL.

4. Keep public payments off until live Stripe links and App Store rules are resolved.

5. Install/activate full Xcode before attempting native iOS build/TestFlight.

6. Run a full native QA pass before App Store submission.

7. Get scholarly/content review for beginner explanations, surah overviews, historical context, and reasons for revelation.

## Instruction For New Codex

Before changing anything:

1. Read this file.
2. Inspect `outputs/NIYYAH-app-public-github-pages/app/index.html`.
3. Inspect `outputs/NIYYAH-app-public-github-pages/app/quran-data.js` only with scripts/tools, not by dumping the full file.
4. Do not claim something is live unless tested.
5. Do not overwrite user/GitHub changes without confirming the target repo and file.
6. Prefer small, verified edits over broad rewrites.
