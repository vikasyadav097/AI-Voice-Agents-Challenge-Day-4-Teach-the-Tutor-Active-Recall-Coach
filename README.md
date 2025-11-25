
---

# 🎓 Day 4 – Teach-the-Tutor: Active Recall AI Coach

A voice-powered **AI tutoring agent** built with **LiveKit Agents**, **Murf AI Falcon TTS**, **Deepgram STT**, and **Google Gemini**, designed to help you learn programming concepts through **active recall** and **interactive teaching**.

This completes **Day 4** of the **#MurfAIVoiceAgentsChallenge**.

---

## 🎯 Key Features

### 🔹 Three Learning Modes

* **Learn Mode**
  The AI explains programming concepts using examples, analogies, and step-by-step breakdowns.

* **Quiz Mode**
  Test your understanding through interactive voice-based questions.

* **Teach-Back Mode**
  You explain a concept to the AI, and it gives structured feedback — perfect for active recall.

### 🔹 Concepts Covered

* Variables
* Loops (for / while)
* Functions
* Conditional Statements (if/else)
* Arrays & Lists

### 🔹 Voice AI Stack

* **Murf Falcon TTS** (en-US-Ryan, conversational style)
* **Deepgram Nova-3 STT**
* **Google Gemini 2.5 Flash** LLM
* Real-time audio via **LiveKit**

---

## 🚀 Quick Start

### **Prerequisites**

* Python **3.9+**
* Node.js **18+**
* LiveKit Server
* API Keys:

  * Murf AI
  * Deepgram
  * Google AI

---

## 🔧 Installation

### **1. Clone Repository**

```bash
git clone https://github.com/GhanshyamJha05/fourth_day_task_murf_api.git
cd fourth_day_task_murf_api
```

---

## 🖥️ Backend Setup

```bash
cd backend
python -m venv .venv
```

Activate environment:

**Windows**

```bash
.venv\Scripts\activate
```

**Mac/Linux**

```bash
source .venv/bin/activate
```

Install dependencies:

```bash
pip install -e .
```

### **Create backend/.env.local**

```
LIVEKIT_URL=ws://127.0.0.1:7880
LIVEKIT_API_KEY=devkey
LIVEKIT_API_SECRET=secret
GOOGLE_API_KEY=your_google_api_key
MURF_API_KEY=your_murf_api_key
DEEPGRAM_API_KEY=your_deepgram_api_key
```

---

## 🌐 Frontend Setup

```bash
cd ../frontend
npm install
```

### **Create frontend/.env.local**

```
NEXT_PUBLIC_LIVEKIT_URL=ws://127.0.0.1:7880
LIVEKIT_API_KEY=devkey
LIVEKIT_API_SECRET=secret
```

---

## ▶️ Running the App

### 1️⃣ Start LiveKit Server

From project root:

```bash
./livekit-server.exe --dev
```

### 2️⃣ Start Backend

```bash
cd backend
.venv\Scripts\activate
python src/agent.py dev
```

### 3️⃣ Start Frontend

```bash
cd frontend
npm run dev
```

### 4️⃣ Open Browser

Go to:
**[http://localhost:3000](http://localhost:3000)**

---

## 🎤 How to Use (Voice Instructions)

1. **Connect** → Click *Connect* & allow microphone
2. **Greet** → Say:
   **“Hello!”**
3. **Choose Mode**

   * “Learn mode”
   * “Quiz mode”
   * “Teach back mode”
4. **Interact** with the tutor
5. **Switch modes anytime** by asking

---

## 🧪 Example Conversations

### **Learn Mode**

* “Explain variables to me.”
* “What are loops?”
* “Teach me functions.”

### **Quiz Mode**

* “Quiz me on variables.”
* “Ask me questions about loops.”

### **Teach-Back Mode**

* “Let me explain functions.”
* “I want to teach loops.”

---

## 📂 Project Structure

```
.
├── backend/
│   ├── src/
│   │   ├── agent.py              # Main agent logic
│   │   └── murf_tts.py           # Murf TTS integration
│   ├── .env.local
│   └── pyproject.toml
│
├── frontend/
│   ├── app/                      # Next.js app
│   ├── components/
│   ├── .env.local
│   └── package.json
│
├── shared-data/
│   └── day4_tutor_content.json   # Learning content
│
└── livekit-server.exe
```

---

## 📝 Tutor Content File

**shared-data/day4_tutor_content.json**

```json
[
  {
    "id": "variables",
    "title": "Variables",
    "summary": "Variables are like labeled containers...",
    "sample_question": "What is a variable and why is it useful?"
  }
]
```

---

## 🗣️ Voice Configuration (Murf Falcon)

* **Voice**: en-US-Ryan
* **Style**: Conversational
* **Sample Rate**: 24 kHz
* **Output**: WAV (Mono)

---

## 🐛 Troubleshooting

### **Agent not responding**

* Ensure all 3 services are running
* Verify API keys
* Check browser console for errors

### **No audio**

* Microphone permission
* Valid Murf API key
* Working speaker device

### **Connection issues**

* LiveKit running on port **7880**
* Firewall not blocking WS
* Correct .env URLs

---

## 🏆 Challenge Completion (Day 4)

✅ Learn / Quiz / Teach-Back Modes
✅ Mode Switching
✅ Murf Falcon TTS
✅ Deepgram STT
✅ Gemini LLM
✅ Real-time Voice Interface

---
| Day      | Status         |
| -------- | -------------- |
| Day 1    | ✅ Completed    |
| Day 2    | ✅ Completed    |
| Day 3    | ✅ Completed    |
| Day 4    | ✅ Completed    |
| Day 5–10 | 🔜 Coming soon |


---

## 🙏 Acknowledgments

* **Murf AI** — for the challenge
* **LiveKit** — for the agents framework
* **Deepgram STT**
* **Google AI**
* Open-source community

---


