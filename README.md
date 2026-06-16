# LexiBridge AI 🌉

Empowering the next billion builders in their own tongue. LexiBridge AI is a multi-modal AI copilot that bridges the gap between global English technical lectures and regional language comprehension.

## Problem Statement
High-quality AI and tech education is almost exclusively in English, creating a massive conceptual barrier for millions of students from non-English medium backgrounds. This causes severe cognitive friction, as students spend hours decoding fast-paced technical English and complex jargon rather than actually understanding the core concepts. Current solutions like auto-generated captions fail on technical terms, and standard translators lack multi-modal context.

## Current Progress
* **Repository Initialization:** Monorepo structure established with separate `frontend` and `backend` directories.
* **Frontend (UI/UX):** Initialized Next.js 14 project with Tailwind CSS. The core video upload dashboard and split-pane translation view are mapped out.
* **Backend Architecture:** FastAPI server initialized with endpoints designed for video processing.
* **AI Integration (In Progress):** Currently implementing the pipeline to route audio through Whisper Large v3 for transcription, and setting up the Gemini 1.5 Pro prompt chains to generate Hinglish/Gujarati analogies for technical jargon.

## Tech Stack
* **AI / ML Layer:** Gemini 1.5 Pro (Multimodal), Whisper Large v3 (Speech-to-Text)
* **Frontend:** Next.js 14, Tailwind CSS
* **Backend:** FastAPI, Python
* **Database / Storage:** Supabase (PostgreSQL & Vector Store for RAG)

## Planned Features
**Must Have (MVP - Currently Building)**
* Video-to-Gujarati/Hindi text summary generation.
* Extraction and vernacular explanation of key technical concepts.

**Should Have**
* Multilingual Q&A bot to allow users to ask questions about the video content in their mother tongue.

**Nice to Have**
* AI-generated vernacular flashcards.
* "Hinglish" voice-over synthesis.

## Setup Instructions

### Prerequisites
* Node.js (v18+)
* Python (3.10+)
* API Keys for Google Gemini and Supabase

### Frontend Setup
1. Navigate to the frontend directory:
   ```bash
   cd frontend
   ```
2. Install dependencies:
    ```bash
   npm install
    ```
3. Run the development server:
   ```bash
    npm run dev
   ```

### Backend Setup
1. Navigate to the backend directory:
    ```bash
    cd backend
   ```
2. Create and activate a virtual environment:
   ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```
3. Install dependencies:
   ```bash
    pip install -r requirements.txt
   ```
4. Set up environment variables in a `.env` file (e.g., `GEMINI_API_KEY`, `SUPABASE_URL`).
5. Start the FastAPI server:
   ```bash
    uvicorn main:app --reload
   ```
