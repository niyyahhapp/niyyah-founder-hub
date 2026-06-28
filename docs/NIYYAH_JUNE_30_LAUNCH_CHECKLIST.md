# NIYYAH June 30 Launch Checklist

Updated: June 24, 2026

Goal:
Prepare NIYYAH for a June 30 launch push.

Reality:
A TestFlight/public-preview launch by June 30 is realistic. A fully approved App Store launch by June 30 depends on Xcode build readiness, Apple Developer enrollment, App Store Connect setup, review submission, and Apple's review timing.

## Fixed Today

- Removed the visible temporary "First download user / Returning user" preview gate.
- First-time users now automatically see the 4-screen first-download onboarding.
- Returning users now automatically see the shorter 2-screen intention entry.
- Added a saved `niyyah-has-entered` flag after onboarding is completed.
- Existing users with meaningful history are treated as returning users.
- Added test override links for internal QA only:
  - `?entry=first`
  - `?entry=returning`

## Apple Developer Fee

Apple Developer Program:
99 USD per membership year.

This is not 99 USD per app. One membership can manage/distribute apps under that account, but the membership renews yearly.

Official source:
https://developer.apple.com/support/compare-memberships/

## Launch Priority

### Must Have Before App Store Submission

1. Native Xcode build opens successfully.
2. App icon is real and all required sizes are present.
3. App name is final: NIYYAH.
4. Bundle identifier is final.
5. Arabic/Qur'an text content is verified.
6. No fake "coming soon" placeholders in main learning flow.
7. Privacy Policy link works.
8. Terms link works.
9. App Store screenshots are ready.
10. App Store description is ready.
11. Age rating/content info is completed honestly.
12. App Review notes explain that NIYYAH is a learning/reflection app and does not generate tafsir or religious rulings.

### Strongly Recommended Before App Store Submission

1. TestFlight beta with at least 3-5 testers.
2. Scholar/teacher/content review for beginner explanations.
3. Check every juz 29 and juz 30 surah for missing/mismatched content.
4. Confirm onboarding, surah picker, ayah flow, tafsir expansion, reflection save, journal, progress, vocabulary, quiz, study circle, and profile all work.
5. Confirm no personal email appears in public-facing app/waitlist flows.

## June 24

- Fix first-download vs returning entry flow.
- Confirm public app preview is not showing temporary gate.
- Make App Store/TestFlight checklist.
- Confirm Apple fee.

## June 25

- Open full Xcode.
- Build on iPhone simulator.
- Fix compile errors.
- Check app icon.
- Check Info.plist.
- Create archive if possible.

## June 26

- Create Apple Developer account/enroll if not already done.
- Create App Store Connect app record.
- Set bundle ID.
- Upload build to TestFlight.
- Add internal testers.

## June 27

- TestFlight smoke test.
- Fix any crash or blocker.
- Finalize App Store screenshots.
- Finalize description, keywords, support URL, privacy URL.

## June 28

- Submit for App Review if native build is stable.
- Keep public waitlist/social launch active.
- Continue gathering waitlist signups and feedback.

## June 29

- Respond to any Apple review issues.
- Prepare launch posts.
- Prepare "NIYYAH is coming soon / join TestFlight" fallback if App Store review is not approved yet.

## June 30

Launch path:

- If App Store approved: announce App Store launch.
- If not approved: announce TestFlight / public preview / waitlist milestone launch.

Do not disappear if App Store approval is delayed. Use the delay as a build-in-public update.

## App Review Notes Draft

NIYYAH is a Qur'an understanding and reflection app for Muslim youth and young adults. The app helps users read Arabic Qur'an text, view translation, learn beginner-friendly surah context and ayah understanding, access source tafsir, reflect through journaling, save vocabulary, complete quizzes, and track progress.

NIYYAH does not alter Qur'anic Arabic. NIYYAH does not generate tafsir, fatwas, or personal religious rulings using AI. The app is a learning and reflection companion, not a replacement for qualified scholars or teachers.

## Public Links

Waitlist:
https://niyyahhapp.github.io/niyyah-waitlist/

Public app preview:
https://niyyahhapp.github.io/niyyah-app/app/?v=full-restore

Private founder hub:
https://niyyahhapp.github.io/niyyah-founder-hub/

Phone founder hub:
http://192.168.68.56:8810/NIYYAH-private-hub-github-pages/
