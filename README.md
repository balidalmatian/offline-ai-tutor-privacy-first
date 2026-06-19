# Offline AI Tutor — Android Application

[![Android](https://img.shields.io/badge/Android-8.0%2B-brightgreen)](https://developer.android.com)
[![Kotlin](https://img.shields.io/badge/Kotlin-1.9.0-purple)](https://kotlinlang.org)
[![License](https://img.shields.io/badge/License-MIT-blue)](LICENSE)
[![Doctoral Research](https://img.shields.io/badge/Doctoral-Research-red)](https://github.com)


## 📖 About This Project

This application is part of a **doctoral research project in Informatics** at the **University of Vigo**, investigating the adoption of Generative AI in higher education across three distinct regions: the Indian Subcontinent, Latin America and the Caribbean, and Europe.

**This Android application is the practical implementation of that research** — a fully offline, privacy-first AI tutor that can be deployed in real-world educational settings.


## 🎯 Research Context

| Aspect | Detail |
|:---|:---|
| Institution | University of Vigo (UVigo), Spain |
| Degree | Doctorate in Informatics / Computer Science |
| Supervisors | Dr. Manuel Pérez Cota, Dr. Agostinho Sousa Pinto |
| Regions Studied | Indian Subcontinent, Latin America & Caribbean, Europe |
| Sample Size | 3,310 students + 83 faculty interviews |
| Core Models | PLS-SEM, ANN, Stacking Ensemble (RF + XGB + MLP + Ridge) |
| Key Variables | Perceived Usefulness (U), Ease of Use (E), Trust (T), Anthropomorphism (A) |


## 🔬 Why This Application Exists

### The Problem

Millions of students worldwide lack reliable internet access, yet cloud-based AI tutoring assumes constant connectivity.

| Region | Internet Access | Key Barrier |
|:---|:---|:---|
| Indian Subcontinent | 33-87% | Power outages, rural isolation |
| Latin America & Caribbean | 39-94% | Unreliable grids, challenging terrain |
| Europe | 80-98% | Occasional rural instability |

**Key findings from the doctoral research:**

- Students show **75% agreement** on continuance intention to use GenAI
- Faculty across all regions express **unanimous intention** to continue using GenAI tools
- **Language bias** is critical: English dominates 89.7% of training data
- **Privacy concerns** are significant across all regions

### The Solution

**Offline AI Tutor** brings AI-powered tutoring directly to the device — no internet, no subscription, no data collection.

> **Mission:** Democratize access to quality education by making AI tutoring available anywhere, anytime — even without internet.


## ✨ Key Features

| Feature | Description |
|:---|:---|
| 🔌 100% Offline | Works without internet after initial model download |
| 🔒 Total Privacy | All data stays on your device — no servers, no tracking |
| 🌍 Multilingual | Automatic language detection (FastText) — 15+ languages |
| 🎮 Gamification | XP, levels, badges, and achievements |
| 📝 Study Tools | Handwriting canvas, focus timer, mood tracker, notes |
| 🤖 AI Tutor | Powered by Gemma 4 for contextual, intelligent responses |
| 📦 Open Source | MIT License — fork, modify, distribute freely |
| 🧠 Predictive Model | Stacking Ensemble (TFLite) for personalized risk assessment |


## 🧠 Architecture

The application follows a three-layer architecture:

**Presentation Layer** (Jetpack Compose UI)

- Welcome → Diagnosis → Dashboard → Chat / Explore

**Logic Layer** (On-Device)

- AI Engine: Gemma 4 + LiteRT (natural language understanding, contextual responses, multi-language support)
- Predictive Model: Stacking Ensemble (TFLite) for risk assessment and personalized recommendations
- Language Detector: FastText (automatic language detection, 15+ languages)

**Data Layer** (Encrypted Local)

- SQLite + SQLCipher (AES-256-GCM)
- User profile, chat history, XP, badges, progress, study notes, flashcards


## 📊 Research Validation

| Validation Method | Details |
|:---|:---|
| Sample Size | 3,310 students across 3 regions |
| Qualitative Data | 83 semi-structured interviews |
| Meta-Analysis | 60+ post-2023 studies synthesized via MASEM |
| Cross-Validation | 10-fold cross-validation for ANN models |
| Cultural Validation | Tested across Indian Subcontinent, LAC, and Europe |
| Predictive Accuracy | R² = 0.91 for Stacking Ensemble |


## 🛠️ Tech Stack

| Component | Technology |
|:---|:---|
| Language | Kotlin |
| UI Framework | Jetpack Compose |
| LLM Model | Gemma 4 (4-bit quantized) |
| Inference Engine | Google LiteRT |
| Predictive Model | Stacking Ensemble (TFLite) |
| Language Detection | FastText (lid.176.bin) |
| Encryption | AES-GCM (Android Keystore) |
| Database | SQLite + SQLCipher |
| Dependency Injection | Hilt |
| Min SDK | Android 8.0 (API 26) |
| Target SDK | Android 14 (API 34) |
| License | MIT |


## 📱 Screens

| Screen | Description |
|:---|:---|
| Welcome | App introduction with privacy notice |
| Diagnosis | 10 Likert-scale questions (1-5) |
| Dashboard | Index display with personalized recommendations |
| AI Chat | Conversation with Gemma 4 — works offline |
| Explore Hub | Handwriting canvas, focus timer, mood tracker, notes |
| Profile | Progress, XP, badges, and settings |


## 🚀 Getting Started

### Prerequisites

- Android Studio Hedgehog or newer
- Android SDK 26+ (Android 8.0)
- Android device with 4GB+ RAM (recommended)
- 2-3GB free storage for model download

Open in Android Studio, sync Gradle, connect a device, and click Run.

On first launch, the app downloads the Gemma 4 model (~2-3GB). After that, go completely offline forever.
### 🔒 Privacy

| Principle | Implementation |
|:---|:---|
| Zero data collection | No data ever leaves your device |
| Encryption at rest | AES-GCM via Android Keystore |
| No accounts | No sign-up required |
| No analytics | No tracking of any kind |
| User control | Delete all data from settings |

All data remains on your device:

- Encrypted SQLite (AES-GCM)
- User profile, chat history, XP, badges, progress
- Study notes, flashcards
- All inference happens locally with Gemma 4 + LiteRT
- No cloud processing


### 🧪 Testing

**Diagnosis:** Launch app, answer 10 questions, dashboard shows your index.

**AI Chat:** Navigate to Chat, ask any academic question, Gemma 4 responds offline.

**Explore Hub:** Try Handwriting Canvas, Focus Timer, or Mood Tracker.


### 📚 References

- Paiva, J. (2025). *The AI Middle Powers: Gen AI Adoption in Higher Education across the Indian Subcontinent, Latin America and the Caribbean, and Europe*. Doctoral Thesis, University of Vigo.
- Pinto, A. S., Abreu, A., Cota, M. P., & Paiva, J. (2025). *The Technology Acceptance Model (TAM): A MASEM Approach*. ICITED25, Springer.
- Pinto, A. S., Abreu, A., Costa, E., Cota, M. P., & Paiva, J. (2025). *Exploring DeepSeek Adoption in Higher Education in Bangladesh*. Q1/Q2 Journal.


### 🤝 Contributing

Contributions welcome. See CONTRIBUTING.md


### 📄 License

MIT License — see LICENSE file for details.


### 🙏 Acknowledgments

- Google DeepMind for Gemma 4
- Google Android Team for LiteRT
- All 3,310 students and 83 faculty participants


### 🔗 Links

- Doctoral Research: https://github.com/your-username/thesis
- Documentation: https://github.com/your-username/offline-ai-tutor/wiki
- Issues: https://github.com/your-username/offline-ai-tutor/issues


---

**Built with ❤️ for learners everywhere.**

> *"Education is the most powerful weapon which you can use to change the world."* — Nelson Mandela
### Building APK

```bash
./gradlew assembleDebug
./gradlew assembleRelease

📂 Project Structure
text
app/
├── src/main/java/com/myapp/
│   ├── MainActivity.kt
│   ├── MainApplication.kt
│   ├── di/
│   │   └── AppModule.kt
│   ├── data/
│   │   ├── UserProfile.kt
│   │   ├── ContentRepository.kt
│   │   ├── local/
│   │   │   ├── Database.kt
│   │   │   ├── Entities.kt
│   │   │   └── Dao.kt
│   │   └── repository/
│   │       └── UserProfileRepository.kt
│   ├── ml/
│   │   ├── Gemma4Engine.kt
│   │   ├── LanguageDetector.kt
│   │   ├── FastTextLanguageDetector.kt
│   │   ├── ModelDownloadManager.kt
│   │   └── Recommender.kt
│   ├── ui/
│   │   ├── navigation/
│   │   │   └── NavGraph.kt
│   │   ├── welcome/
│   │   │   ├── WelcomeScreen.kt
│   │   │   └── WelcomeViewModel.kt
│   │   ├── diagnosis/
│   │   │   ├── DiagnosisScreen.kt
│   │   │   └── DiagnosisViewModel.kt
│   │   ├── dashboard/
│   │   │   ├── DashboardScreen.kt
│   │   │   └── DashboardViewModel.kt
│   │   ├── chat/
│   │   │   ├── ChatScreen.kt
│   │   │   └── ChatViewModel.kt
│   │   ├── explore/
│   │   │   └── ExploreScreen.kt
│   │   ├── canvas/
│   │   │   └── CanvasScreen.kt
│   │   ├── timer/
│   │   │   └── TimerScreen.kt
│   │   ├── mood/
│   │   │   ├── MoodScreen.kt
│   │   │   └── MoodViewModel.kt
│   │   ├── notes/
│   │   │   ├── NotesScreen.kt
│   │   │   └── NotesViewModel.kt
│   │   ├── flashcards/
│   │   │   ├── FlashcardsScreen.kt
│   │   │   └── FlashcardsViewModel.kt
│   │   └── profile/
│   │       ├── ProfileScreen.kt
│   │       └── ProfileViewModel.kt
│   └── utils/
│       ├── Constants.kt
│       ├── Security.kt
│       ├── Gamification.kt
│       └── LocaleHelper.kt
├── src/main/assets/
│   ├── gemma_4_4bit.tflite
│   ├── ensemble_model.tflite
│   └── lid.176.bin
└── build.gradle.kts


### Installation

```bash
git clone https://github.com/your-username/offline-ai-tutor.git
cd offline-ai-tutor
