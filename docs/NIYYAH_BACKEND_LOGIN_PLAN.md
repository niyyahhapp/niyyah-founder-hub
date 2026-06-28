# NIYYAH Backend and Login Plan

Draft status: recommendation before implementation.

## Why We Need This

If NIYYAH only stores journal entries and progress locally, a user who deletes the app may lose:

- Journal reflections.
- Personal duas.
- Favorite ayahs.
- Vocabulary history.
- Memorization progress.
- Completed ayah progress.

So yes, long-term NIYYAH needs backup/sync.

## Important Product Rule

Do not force login on first open.

NIYYAH should allow users to start calmly as a guest, then offer optional account backup:

"Save your reflections across devices"

This protects the calm onboarding experience and avoids making the app feel like a social platform.

## Recommended Auth Options

### Option A: Sign in with Apple + iCloud/CloudKit

Best for:

- iPhone-first launch.
- Privacy.
- Lower cost.
- Less backend complexity.

Tradeoff:

- Does not support Google login in the same way.
- Works best inside the Apple ecosystem.

### Option B: Supabase Auth + Database

Best for:

- Sign in with Apple.
- Sign in with Google.
- Cross-platform future.
- A real backend database.

Tradeoff:

- Requires backend security rules.
- Requires careful privacy handling.
- Adds more launch complexity.

### Option C: Firebase Auth + Firestore

Best for:

- Google login.
- Fast setup.
- Common mobile backend.

Tradeoff:

- More Google ecosystem dependence.
- Security rules must be correct.
- Can become messy if not planned carefully.

## Recommendation

For NIYYAH:

1. Keep guest mode.
2. Add "Back up my journal" as an optional account feature.
3. Start with Sign in with Apple.
4. Add Google login only if we choose Supabase or Firebase.
5. Store only the minimum needed data.

## App Store Rule To Remember

If an app offers third-party social login such as Google, Apple generally requires Sign in with Apple as an equivalent option unless an exception applies.

That means:

- Google login alone is not a good App Store plan.
- Sign in with Apple should be included if Google login is included.

## Suggested User Data Model

User:

- id
- createdAt
- authProvider

Reflection:

- id
- userId
- ayahReference
- prompt
- reflectionText
- duaText
- createdAt
- updatedAt

FavoriteAyah:

- id
- userId
- ayahReference
- translation
- savedAt

VocabularyWord:

- id
- userId
- word
- meaning
- context
- learnedAt

Progress:

- userId
- completedAyahs
- memorizationStatusBySurah
- streak
- updatedAt

## Data Safety Rules

- Do not store unnecessary personal data.
- Do not store location.
- Do not sell data.
- Keep journal entries private by default.
- Give users a way to delete account data before public launch.
- Add Privacy Policy updates before enabling backend sync.

## Build Order

1. Finish current app QA and content review.
2. Choose backend: CloudKit, Supabase, or Firebase.
3. Add optional account screen.
4. Add Sign in with Apple.
5. Add cloud sync for journal/progress.
6. Add account deletion.
7. Update Privacy Policy and Terms.
8. Test with TestFlight.
