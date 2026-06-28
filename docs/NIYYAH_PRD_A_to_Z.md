# NIYYAH Product Requirements Document

## Product Summary
NIYYAH is a calm Qur'an reflection app for Muslim youth and young adults who recite Qur'an but want help understanding meaning, context, and life lessons in a simple way. The app is not a tafsir generator and does not alter Qur'anic Arabic. It organizes verified Qur'an text, translation, source tafsir, and beginner-friendly learning prompts into a guided reflection experience.

## Current MVP Scope
- Platform: SwiftUI iOS app plus local browser preview.
- Content: Al-Fatihah, Juz 28, Juz 29, and Juz 30.
- Current dataset: 1,139 ayahs across 58 surahs.
- Offline-first: all imported content is stored locally in JSON.
- No login, backend, social features, or network dependency in the MVP runtime.

## Target Users
- Muslim youth and young adults.
- Users who may recite or memorize Qur'an but do not fully understand context.
- Beginners who need calm structure, not dense scholarly walls of text.
- Users who benefit from soft UI, emotional safety, guided reflection, and simple language.

## Product Philosophy
NIYYAH should feel like a gentle teacher guiding the user through the Qur'an one ayah at a time. The experience should help users understand:
- What the surah is about.
- Why/context in which the surah was revealed, where available.
- What each ayah means in simple language.
- What the ayah teaches practically.
- How to reflect and make dua from what they read.

## Content Sources
- Arabic Qur'an text: Quran.com / Quran Foundation API import.
- Translation: Saheeh International via Quran.com API.
- Source tafsir: Ibn Kathir (Abridged) via Quran.com API where available.
- Some source tafsir passages are grouped across multiple ayahs. The UI labels these as shared passages instead of pretending each ayah has unique source tafsir.
- Beginner summaries and ayah understanding fields are simplified educational summaries based on imported translation/source tafsir structure and should be reviewed by a qualified Islamic reviewer before production.

## Core Screens

### Home
- Shows NIYYAH branding.
- Shows current ayah preview.
- Shows day streak and completed ayah count.
- Continue Reflection button.
- Begin New Session button.
- Searchable surah picker.
- Surah picker grouped by:
  - Al-Fatihah
  - Juz 28
  - Juz 29
  - Juz 30

### Surah Start
Shown before starting a selected surah.
- Bismillah.
- Dua: Rabbi Zidni 'Ilma.
- English meaning: My Lord, increase me in knowledge.
- Surah Overview card:
  - Surah name.
  - Main theme.
  - Historical context.
  - Why it was revealed.
  - Key lessons.
  - Source.

### Ayah Reading
- Arabic ayah is the visual focus.
- Translation appears below.
- Shows progress within current surah.
- Controls:
  - Back.
  - Previous Ayah.
  - Understand.
  - Reflect.
  - Next Ayah.

### Ayah Understanding
Displayed when the user taps Understand.
- Simple Meaning.
- What This Teaches Us.
- Connection to the Surah.
- Source tafsir passage label:
  - Example: Shared tafsir passage for Al-Mujadila 58:2-4.
- Read Source Tafsir expandable button.
- Source tafsir is hidden by default to avoid overwhelming beginners.

### Reflection
- Guided prompt.
- Free-form reflection text area.
- Optional dua text area.
- Save Reflection.
- Reflection saved confirmation.

### Journal
- Saved reflections organized by ayah.
- Shows prompt, reflection, dua, date, and ayah reference.
- Local storage only in preview; local document persistence in SwiftUI.

### Progress
- Percent complete.
- Completed ayah count.
- Day streak.
- Journal entries.
- Current ayah context.

### Surah Completion
Shown after completing a surah.
- Congratulatory completion state.
- Gentle dua/blessing.
- Continue to next surah.
- Choose another surah.

## Current Implemented Features
- Searchable surah picker.
- Grouped library sections.
- Ayah-by-ayah navigation.
- Back and Previous Ayah controls.
- Surah overview before start.
- Ayah understanding cards.
- Full source tafsir accordion.
- Quran Word Explainer for selected glossary terms.
- Local Quran Vocabulary bank.
- Reflection journaling.
- Local saved reflections.
- Favorite ayahs.
- Progress tracking.
- Simple memorization status by surah:
  - Not Started.
  - Learning.
  - Memorized.
- Quick surah quiz after completion.
- "Did You Understand This Surah?" completion summary.
- Key Lessons Review card.
- Finish-surah message.
- Short, beginner-first tafsir experience.

## Design Direction
- Soft, calm, feminine but not romantic or flashy.
- Pastel warmth: cream, blush, peach, rose, cocoa, olive.
- Glass/blur cards.
- Spacious layout.
- Large centered Arabic.
- Minimal cognitive load.
- More teacher-like than academic.

## Current QA Results
- Preview tests passed.
- Data integrity checks passed.
- 1,139 ayahs verified.
- 58 surahs verified.
- First ayah: Al-Fatihah 1:1.
- Last ayah: An-Nas 114:6.
- No duplicate ayah IDs.
- No missing Arabic text.
- No missing translation.
- No missing source tafsir.
- No missing ayah simple meaning.
- No missing practical lesson.
- No missing connection field.
- No missing surah overview fields.
- Key short surahs now have distinct ayah-level simple meanings:
  - Al-Fatihah.
  - Al-Fil.
  - Al-Kafirun.
  - Al-Ikhlas.
  - Al-Falaq.
  - An-Nas.

## Known Product Risks / Gaps
- Beginner summaries are not a replacement for scholarly tafsir and need Islamic review.
- Quran.com source tafsir is often grouped by passage, so many ayahs share the same source tafsir passage.
- SwiftUI app has the main ayah understanding UI, but the browser preview is currently the most complete product prototype for surah start/finish flow.
- The Clear Quran translation was not imported because an authorized API/source was not confirmed.
- Abdel Haleem translation may be considered later as a simpler translation option.
- Full production app still needs real iOS build verification in Xcode.

## Future Features
- Translation selector.
- Audio recitation.
- Bookmark/favorite ayahs.
- Better streak logic based on actual dates.
- Islamic scholar/content review workflow.
- Export/share private journal entries.
- Limited Learning Assistant only after structured features are stable.
  - Allowed: explain words, simplify tafsir, summarize ayahs, explain concepts.
  - Not allowed: fatwas, personal rulings, marriage advice, medical advice, political opinions, open-ended life advice.

## Success Criteria
- User can choose a surah.
- User understands the surah theme before reading.
- User can move ayah by ayah without confusion.
- User sees simple meaning before source tafsir.
- User can reflect and save a journal entry.
- User can finish a surah and feel encouraged.
- App feels calm, clear, and emotionally safe.
