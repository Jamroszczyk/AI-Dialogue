Here’s a polished, user-friendly README.md draft for your repo:

⸻

AI Dialogue

Two AI agents talking to each other — in real time, out loud, right on your machine.

AI Dialogue is a local-first app where you set a short system prompt for each of two AI agents, hit Go, and watch them debate, role-play, or brainstorm in real time.
While they speak, you’ll see:
	•	🎙 Low-latency speech via on-device Piper TTS
	•	📡 Live updates streamed over WebSockets
	•	🔵 Circular audio visualizers showing who’s talking
	•	☁ Dynamic word cloud highlighting key terms (stopwords filtered out)

Great for prototyping conversations, testing UX copy, language learning, safety research, or just having fun with simulated debates.

⸻

✨ Features
	•	Two configurable agents with independent system prompts
	•	On-device speech (Piper TTS + ONNX voices — no cloud latency)
	•	Azure OpenAI GPT-4o mini backend (via FastAPI)
	•	WebSocket event streaming for smooth UI updates
	•	Modern React frontend with responsive layout
	•	Built-in guardrails — prompt length and turn limits

⸻

📦 Requirements
	•	Python ≥ 3.9
	•	Node.js ≥ 18 (for frontend build)
	•	Azure OpenAI credentials (GPT-4o mini deployment)
	•	On-device Piper TTS voice files (download separately)

⸻

🔧 Installation

1. Clone the repo

git clone https://github.com/yourusername/ai-dialogue.git
cd ai-dialogue

2. Backend setup (FastAPI + Piper TTS)

python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install --upgrade pip
pip install -r requirements.txt

3. Frontend setup (React UI)

cd frontend
npm install
npm run build
cd ..

4. Environment variables

Create a .env file in the project root:

AZURE_OPENAI_API_KEY=your_api_key_here
AZURE_OPENAI_ENDPOINT=https://your-resource-name.openai.azure.com/
AZURE_OPENAI_DEPLOYMENT=gpt-4o-mini
PIPER_VOICE=voice-file.onnx

5. Run the app

uvicorn main:app --reload

Backend will serve API + WebSocket. Frontend build is served from /frontend/dist.

⸻

📜 Requirements file (Python)

Key packages:

fastapi==0.116.1
uvicorn==0.35.0
websockets==15.0.1
python-dotenv==1.1.1
pydantic==2.11.7
transformers==4.55.1
piper-tts==1.3.0
numpy==2.3.2
pygame==2.6.1
pillow==11.3.0

Full requirements.txt includes exact versions for reproducibility.

⸻

🖥 Stack
	•	Backend: FastAPI + WebSockets
	•	Frontend: React + Web Audio API + Canvas
	•	TTS: Piper (ONNX runtime)
	•	LLM: Azure OpenAI GPT-4o mini

⸻

📄 License

MIT — use freely, just credit the project.

⸻

Do you want me to also create a requirements.txt file containing exactly the versions you listed so it’s ready to drop in the repo? That way the README’s install steps will match perfectly.
