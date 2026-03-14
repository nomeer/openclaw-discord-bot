# openclaw-discord-bot

# 🖤 DarkSoulBot — AI Discord Bot Portfolio

> A fully self-hosted, AI-powered Discord bot built on [OpenClaw](https://github.com/openclaw/openclaw) with voice, STT, live data, and more.

---

## 🧠 What I Built

**DarkSoulBot** is a personal AI assistant deployed directly inside a Discord server. It's not a simple command bot — it's a full reasoning AI agent that can hold conversations, fetch live data, generate voice, and transcribe speech in real time.

---

## ⚙️ Tech Stack

| Layer | Technology |
|---|---|
| AI Agent Runtime | [OpenClaw](https://github.com/openclaw/openclaw) |
| AI Model | Anthropic Claude Sonnet 4.6 |
| Text-to-Speech | Microsoft Edge TTS (`edge-tts`) |
| Speech-to-Text | `faster-whisper` (local, CPU) |
| Secondary AI | Google Gemini API |
| Whisper API | OpenAI Whisper API |
| Voice (ElevenLabs) | SAG (ElevenLabs TTS) |
| Platform | Discord (Bot Token) |
| Host | Self-hosted on Windows WSL2 (Linux) |

---

## 🚀 Features Built & Tested

### 🎮 Steam Market Price Checker
- Live item price lookups via Steam Community Market API
- Tested with: Kilowatt Case, Dreams & Nightmares Case
- Real-time lowest price, median price, and 24h volume

### ☁️ Weather Queries
- Current temperature, feels-like, humidity, wind speed
- Powered by wttr.in API
- Tested with: Rawalpindi, Pakistan

### 🎙️ Text-to-Speech (Edge TTS)
- Converts any text to an audio file using Microsoft Edge TTS
- Sends audio directly as a Discord attachment
- Multiple voices available (e.g. `en-US-GuyNeural`)

### 👂 Speech-to-Text (Faster Whisper)
- Transcribes Discord voice messages using `faster-whisper`
- Runs fully locally on CPU — no cloud needed
- Supports multiple languages (Arabic, English, Urdu, etc.)

### 🤖 Discord Member Management
- Fetches full server member list via Discord API
- Attempted inactive member detection (30-day filter)
- Bot permission scoping: member reads vs message history

### 💬 Thread-Based Conversations
- Configured mention-free replies in specific Discord threads
- Bot responds to all messages in a thread without `@mention`

### 🔍 Live Data & APIs
- Steam Market API
- wttr.in Weather API
- Discord REST API (members, messages, reactions)
- Epic Games free games API

---

## 🧪 What I Learned

### AI Agent Architecture
- How OpenClaw works as an AI agent runtime
- How to configure an agent with memory, skills, and tools
- How session context and memory files persist across restarts

### Discord Bot Development
- Discord REST API (Bot token auth, guild members, channels)
- Sending files/audio as Discord attachments
- Bot permission scopes and their limitations (403 errors)
- Thread vs channel behavior for bots

### Voice Pipeline
- Installing and using `edge-tts` for TTS generation
- Using `faster-whisper` for local STT (lighter than openai-whisper)
- Converting voice messages to text and vice versa
- Audio format handling (OGG Opus → MP3)

### Self-Hosting AI
- Running an AI bot on WSL2 (Linux on Windows)
- Managing Python packages for AI workloads
- Understanding model size tradeoffs (tiny vs small vs medium Whisper)
- API key management for multiple AI providers

### Security Mindset
- Why bots shouldn't expose shell access in public channels
- Principle of least privilege for bot permissions
- Keeping private data out of group chat contexts

---

## 📁 Project Structure

```
OpenClaw Workspace/
├── SOUL.md          # Bot personality & behavior
├── MEMORY.md        # Long-term memory
├── memory/          # Daily session logs
│   └── 2026-03-15.md
├── USER.md          # Owner profile
├── TOOLS.md         # Tool configurations
└── HEARTBEAT.md     # Periodic task scheduler
```

---

## 🔮 What's Next

- [ ] Better Whisper model (upgrade tiny → small for accuracy)
- [ ] Gemini API integration for multimodal tasks
- [ ] Read Message History permission for activity tracking
- [ ] Inactive member detection & moderation tools
- [ ] ElevenLabs TTS for more natural voice output

---

## 👤 Built By

**Nomeer Sheikh** ([@nomeer](https://github.com/nomeer))
Self-hosted AI enthusiast • Discord bot builder • OpenClaw explorer

---

> *"I didn't just install a bot. I built a thinking assistant that lives in my Discord server."*
