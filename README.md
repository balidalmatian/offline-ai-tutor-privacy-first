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

### Installation

```bash
git clone https://github.com/your-username/offline-ai-tutor.git
cd offline-ai-tutor
