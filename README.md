GenAI Healthcare Voice Assistant for Clinic Front Desk
by Mahsan Zare
May 16, 2025


This is a self-contained project demonstrating a voice-enabled AI assistant for healthcare adminstrative tasks, including appointment scheduling and insurance verification. The assistant uses Generative AI and Voice AI technologies for natural conversation.
The clinic for this task was a cardiology clinic called Chamber Cardiology Clinic. 

Project Overview

This assistant simulates a front-office phone call where the user speaks (or plays a pre-recorded .mp3 file), and the AI responds with synthesized voice output. The system uses:

OpenAI GPT-4o for natural language generation

OpenAI Whisper for speech-to-text (STT)

ElevenLabs for text-to-speech (TTS)

All logic is orchestrated in a single runnable Python script.


Setup Instructions

1. Clone the repository

git clone https://github.com/YOUR_USERNAME/aivoiceassistant.git
cd aivoiceassistant

2. Create a virtual environment (optional but recommended)- I used VS Visual Code for IDE.

python3 -m venv venv
source venv/bin/activate

3. Install dependencies

pip install -r requirements.txt

4. Add your API keys

Create a .env file by copying the template:

cp .env.example .env

Then update .env with your own API keys:

OPENAI_API_KEY=your_openai_key_here
ELEVENLABS_API_KEY=your_elevenlabs_key_here

Do not commit .env: It is excluded by .gitignore.

How to Run the Demo

Ensure you have at least one user input file in 02_audio/first_scenario/input/ named:

user_input_1.mp3
user_input_2.mp3

Start the assistant in the terminal:

python 01_voice_orchestration/app.py

The assistant will:

Speak a greeting

Wait for your .mp3 file (press Enter to proceed)

Transcribe your input using Whisper

Generate a response using GPT-4o

Speak the response aloud using ElevenLabs

Repeat the process for the next file

Assistant responses are saved in the output/ folder as .mp3 files. 

Here is the full demo: 

https://github.com/user-attachments/assets/03e7d3ae-6328-43d0-b7c6-5d165d598a53

Audio Recordings: 

Scenario #1: Appointment Scheduling

Scenario #2: Hours & Location Confirmation & Insurance Verification (Denial Flow) 





