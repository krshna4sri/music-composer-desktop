An intelligent AI-assisted music composition platform built with Electron (React) + FastAPI (Python).

This project combines rule-based music theory, probabilistic generation, stochastic creativity, and Retrieval-Augmented Generation (RAG) to create a next-generation composing environment.

🚀 Vision

To build a MuseScore-like notation software enhanced with intelligent compositional assistance where users can:

Create scores (Grand Staff, String Quartet, SATB, etc.)

Generate stylistic ideas (e.g., “Compose like Bach”)

Automatically validate counterpoint and voice-leading

Repair rule violations

Ask theory questions in context

Co-compose with AI instead of using disconnected tools

🧱 Core Foundations

This system integrates four compositional pillars:

1️⃣ Stochastic Composition Engine

Generates motifs, melodic seeds, and rhythmic sketches using probabilistic logic.

2️⃣ Markov Style Engine

Learns stylistic transitions from corpora and produces phrase-level continuation in a chosen style (e.g., Bach, Mozart, Beethoven).

3️⃣ Constraint & Repair Engine (CR-Counter)

Enforces:

Species counterpoint rules

Raga constraints

Voice-leading correctness

Dissonance control

Auto-repair suggestions

4️⃣ MusicLibRAG (Ollama + FAISS)

Retrieval-Augmented Generation over music theory sources:

Explains rule violations

Suggests cadences

Provides theory-grounded guidance

Answers contextual compositional questions

🖥 Application Architecture
Frontend

Electron

React + TypeScript

OpenSheetMusicDisplay (MusicXML rendering)

Tone.js (audio playback)

Backend

FastAPI

Pydantic (ScoreJSON canonical model)

Ollama (local LLM)

FAISS (vector retrieval)

📁 Project Structure
apps/
  desktop/        → Electron + React UI

services/
  backend/        → FastAPI backend
    api/          → REST endpoints
    core/         → Score model + converters
🧠 Core Data Model

The system uses a canonical ScoreJSON format as the single source of truth:

Notes

Parts

Voices

Time signature

Key signature

Metadata

ScoreJSON → converted to MusicXML → rendered in the UI.

This allows:

Engine integration

Rule validation

Export compatibility

⚙️ Development Setup (Windows)
1️⃣ Backend
cd services/backend
python -m venv .venv
.venv\Scripts\activate
pip install -r requirements.txt
python -m uvicorn app.main:app --host 127.0.0.1 --port 8765 --reload
2️⃣ Desktop App
cd apps/desktop
npm install
npm run dev
🎯 Current MVP Features

Project templates (Grand Staff, String Quartet)

ScoreJSON model

MusicXML rendering

Basic note insertion

RAG panel (stubbed, ready for integration)

🛣 Roadmap
Phase 1 – Foundation

 Desktop scaffold

 Template-based score creation

 MusicXML rendering

 Playback refinement

Phase 2 – Intelligence Integration

 Stochastic engine integration

 Markov style continuation

 CR-Counter validation

 Auto-repair system

Phase 3 – Explainable Composition

 RAG integration with Ollama

 Rule explanation panel

 Context-aware suggestions

Phase 4 – Advanced Composition System

 Multi-voice editing

 Real-time rule highlighting

 Plugin architecture

 Advanced engraving

 Model training pipeline

🎼 Long-Term Goal

To build a compositional operating system that unifies:

Human creativity

Formal music theory

Probabilistic modeling

AI-assisted reasoning

Explainable composition
