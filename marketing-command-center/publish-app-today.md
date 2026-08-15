# NIYYAH Free Launch: Baby Steps

You can prepare and submit NIYYAH today. Apple controls review timing, so submission today does not guarantee that the app becomes public today.

## Part 1 - Keep the Launch Free

1. Open App Store Connect.
2. Open **Niyyah Quran Companion**.
3. Open **Pricing and Availability**.
4. Confirm the app price is **Free**.
5. Open the monthly and yearly subscriptions.
6. Do not add either subscription to the app-version submission.
7. Leave the subscription drafts alone for a later version.
8. In Xcode, confirm this build has no visible purchase or restore buttons. The NIYYAH code is already configured for free-beta access, but you must visually test the archive you upload.

## Part 2 - Final Test on Your iPhone

1. Connect your iPhone to the Mac with a cable.
2. Unlock the iPhone and tap **Trust** if asked.
3. Open the NIYYAH Xcode project.
4. At the top of Xcode, select the NIYYAH scheme.
5. Select your real iPhone as the destination.
6. Press the Play button.
7. Test these exact actions:
   - Fresh launch opens.
   - Onboarding or first-run flow can be completed.
   - Home screen loads.
   - A surah opens.
   - An ayah displays correctly.
   - Verified recitation plays inside the app.
   - Pause works.
   - Moving to another ayah stops the previous audio.
   - Source Tafsir opens where available.
   - No Source Tafsir button opens a blank page.
   - Reflection saves.
   - Journal reopens the saved reflection.
   - Vocabulary saves a word.
   - Progress updates.
   - A Circle can be created.
   - A second account can join with a code.
   - Sign in, sign out, and sign back in work.
   - Account deletion request works.
   - Sources & Trust opens.
   - Feedback opens.
   - No Plus paywall or Restore Purchases button is visible.
8. If any item fails, stop and fix it before uploading.

## Part 3 - Archive and Upload

1. In Xcode, choose **Any iOS Device (arm64)** as the destination. Do not choose a simulator.
2. In the menu bar, click **Product**.
3. Click **Archive**.
4. Wait for the Organizer window.
5. Select the newest NIYYAH archive.
6. Click **Distribute App**.
7. Choose **App Store Connect**.
8. Choose **Upload**.
9. Keep automatic signing selected unless Xcode shows a signing error.
10. Continue through validation.
11. If validation passes, click **Upload**.
12. Wait for the upload success message.
13. Wait for Apple's processing email. The build may not appear immediately.

## Part 4 - Complete App Store Connect

1. Open App Store Connect.
2. Open **Niyyah Quran Companion**.
3. Open **iOS App Version 1.0**.
4. Upload the iPhone screenshots.
5. Because the app supports iPad, upload the required iPad screenshots too.
6. Paste the final promotional text, description, keywords, support URL, version, and copyright from the approved NIYYAH App Store copy document.
7. Set the Support URL to the public NIYYAH support or feedback page.
8. Set the Marketing URL to the public NIYYAH page.
9. Under **Build**, click the plus button and select the processed build.
10. Answer export-compliance questions truthfully. Do not guess if the screen asks about encryption you do not understand.
11. Under **App Review Information**, add your real contact details.
12. If review can use the app without signing in, turn off **Sign-in required** and explain that sign-in is optional for Circles/sync.
13. If Apple must sign in to test Circles, provide a dedicated review account that contains no personal data.
14. In Review Notes, explain:
   - Core reading works without payment.
   - The beta is free.
   - Account creation is optional unless required for Circles/sync.
   - Where the reviewer can find Sources & Trust, Feedback, and account deletion.
   - How to create and join a Circle.
15. Select **Manually release this version** so you control the exact public launch moment.

## Part 5 - App Privacy

1. In the app sidebar, open **App Privacy**.
2. Add the public privacy-policy URL.
3. Answer the data questions based on what the shipped build and all included SDKs actually collect.
4. Include Supabase authentication and any diagnostics used by the build.
5. Do not select **No data collected** merely because the app is free.
6. Publish the privacy answers.

## Part 6 - Availability

1. Open **Pricing and Availability**.
2. Keep the app free.
3. Select the countries and regions you are ready to support.
4. If you do not want an EU launch yet, deselect EU member states before submission.
5. Remember that limiting availability does not replace privacy, safety, or legal compliance elsewhere.

## Part 7 - Submit

1. Return to **iOS App Version 1.0**.
2. Check that every required field is complete.
3. Confirm the correct build is selected.
4. Confirm no subscription is attached.
5. Click **Add for Review**.
6. Open the draft submission.
7. Click **Submit for Review**.
8. The status should become **Waiting for Review**.
9. Monitor App Store Connect and email for questions from Apple.
10. Reply clearly if Apple asks how sign-in, deletion, Circles, sources, or the free-beta model works.

## Part 8 - Marketing While Apple Reviews

1. Put the public NIYYAH link in every social bio.
2. Prepare Day 1's three posts from this campaign.
3. Send creator scripts to five small Muslim creators whose audience genuinely fits NIYYAH.
4. Contact three MSAs, two Muslim schools or youth groups, and five friends/family beta testers.
5. Ask for one action only: test NIYYAH and report what is confusing.
6. Do not announce "available on the App Store" until the store page is actually live.
7. While waiting, say **submitted to Apple** or **free beta opening soon**.

## What Is Still Outside Codex's Control

- Apple processing the uploaded build.
- Apple's App Review decision and timing.
- Your answers to legal, tax, privacy, and identity questions.
- Final verification on your physical iPhone and iPad.
- Pressing Submit for Review in your authenticated App Store Connect account.

