# NIYYAH Security Review Setup

## Best Setup

Use two layers:

1. A security scanner such as Aikido for secrets, dependency issues, vulnerable packages, and security mistakes.
2. CodeRabbit for pull request review and code-quality comments.

These tools do different jobs. CodeRabbit is useful, but it should not be the only cybersecurity gate before launch.

## What I Can Run Locally Right Now

I ran a local pre-launch check for:

- Missing app data.
- Broken JSON.
- Broken JavaScript syntax.
- Weak public placeholders.
- Secret-looking keys.
- Personal email/name strings in the public waitlist files.
- Dangerous JavaScript patterns.
- Accidental login/auth/network dependencies in the app.

Latest report:

`outputs/NIYYAH_PRELAUNCH_AUDIT_JUNE10.md`

## What Needs GitHub

CodeRabbit and Aikido should be connected after the NIYYAH app code is in GitHub.

Recommended flow:

1. Create a private GitHub repo for the app code.
2. Push the SwiftUI app and preview files.
3. Install Aikido on the repo.
4. Install CodeRabbit on the repo.
5. Make every change through a pull request.
6. Do not merge until local checks, Aikido, CodeRabbit, and manual content review pass.

## App Store Gate

Before App Store submission, run:

- Full Xcode build.
- iPhone simulator walkthrough.
- Real-device TestFlight build.
- Manual content review for Qur'an learning fields.
- Privacy review for local storage and waitlist/email collection.
