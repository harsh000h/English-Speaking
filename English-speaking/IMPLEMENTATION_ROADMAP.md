# English Speaking — implementation roadmap

## Completed in the prototype
- Modern mobile UI and 10-minute daily plan
- First-time grammar and speaking level test
- Beginner, Intermediate, and Advanced results
- Conversation topics and gentle corrections
- AI feedback backend (`/api/chat`)
- Neural voice backend (`/api/tts`) with Ava, Leo, Smriti, and Alex personalities
- Voice speed, accent, preview, and text-only settings
- Repeat-after-me practice
- PWA/offline shell
- Basic microphone privacy messaging

## Production work required

### 1. Pronunciation scoring
Integrate Azure Speech Pronunciation Assessment. Required secrets:
- `AZURE_SPEECH_KEY`
- `AZURE_SPEECH_REGION`

Send a short recording to the backend and return accuracy, fluency, completeness, and prosody scores. Never expose the key in the browser.

### 2. Audio controls
Store recordings only temporarily by default. Add replay and delete controls; require explicit consent before cloud storage.

### 3. Better placement test
Add read-aloud, picture description, 30-second free speaking, and grammar questions. Calculate a level from multiple signals rather than word count alone.

### 4. Progress storage
Use Supabase or Firebase for level, minutes, streak, mistakes, phrases, and voice preferences. LocalStorage is only a prototype fallback.

### 5. Accounts
Add email/Google login, password reset, session expiry, and account deletion.

### 6. Personalization
Use level, goal, difficult skill, and history to select topic, vocabulary, speed, and correction intensity.

### 7. Conversation memory
Store only learning preferences and aggregated mistakes by default. Make transcript retention opt-in and deletable.

### 8. Reminders
Add Android notifications first, then web notifications. Store time zone, schedule, and opt-out state.

### 9. Confidence mode
No interruption or score while speaking; show encouragement and corrections only after the answer finishes.

### 10. Challenge mode
Faster voice, longer answers, no translation, fewer corrections, and optional natural follow-up questions.

## Recommended build order
1. Pronunciation scoring
2. Real progress storage
3. Better placement test
4. Personalized lessons
5. Accounts
6. Reminders and notifications
7. Confidence and challenge modes

The remaining items need a provider decision and API credentials before production integration. The current app runs safely without them using local/demo fallbacks.