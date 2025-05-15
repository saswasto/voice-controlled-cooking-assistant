Tech Stack
Frontend: React Native (or Flutter if you prefer Dart)

Backend: Node.js with Express

Voice APIs:

Web Speech API: For voice recognition and synthesis in real-time

OpenAI Whisper API: For accurate transcription (especially useful for complex or noisy commands)

Database: Firebase Firestore

State Management: Redux (or MobX as an alternative)

Core Features
1. Voice Command Activation
Passive listening (toggleable for privacy)

Trigger phrases like: “Start recipe,” “Next step,” “Set timer for 5 minutes,” etc.

Whisper API fallback for offline/local use or higher accuracy

2. Step-by-Step Cooking Instructions
Fetch and read aloud one instruction at a time

Voice command: “Next,” “Repeat,” or “Go back”

Visual UI with progress tracking

3. Smart Timer Integration
If instruction includes timing, automatically start a timer

Use voice prompts: “Timer done” → auto-transition to next step

Option to say “Pause timer” or “Restart step”

4. Voice-Saved Recipes
Say “Save this recipe” or “I liked it”

Store into Firestore under user’s saved list

Can retrieve with “Show my saved recipes”

5. Hands-Free Sharing
Voice command like “Share this recipe with [contact/email]”

Uses Firebase Functions + email/WhatsApp API (optional)

 System Architecture
Frontend (React Native)

Voice interface (Web Speech API)

Redux for app state: current step, timer, saved recipes

Timer component with voice triggers

Firestore integration for data fetching/saving

Backend (Node.js + Express)

Whisper API integration for transcribing voice

Recipe management APIs

Optional: Auth, analytics, sharing services

Firebase Firestore

Stores recipes, user preferences, saved items

Could support real-time updates (e.g., collaborative cooking)
