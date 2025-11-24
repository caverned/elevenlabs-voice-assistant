# ElevenLabs Voice Assistant

A conversational AI voice assistant built with ElevenLabs' Conversational AI API. This project enables natural voice conversations with an AI agent that can understand context, respond intelligently, and maintain conversation flow.

## Features

- **Real-time Voice Conversation**: Speak naturally with the AI assistant through your microphone
- **Intelligent Response Handling**: The assistant processes your speech and generates contextual responses
- **Interrupt Detection**: Can detect when you interrupt and adjust responses accordingly
- **Custom Agent Configuration**: Personalize the assistant with custom prompts and behavior
- **Transcript Logging**: View real-time transcripts of both user input and agent responses

## How It Works

1. 🎤 Records your voice through the microphone
2. 🖨️ Processes speech to detect when you've finished speaking or are interrupting
3. 🤖 Sends your input to an LLM model to generate intelligent responses
4. 📈 Synthesizes the AI response into natural-sounding speech
5. 🔊 Plays the synthesized speech through your speakers

## Prerequisites

- Python 3.8 or higher
- ElevenLabs account with Conversational AI access
- Microphone and speakers/headphones

## Installation

1. Clone this repository:
```bash
git clone https://github.com/caverned/elevenlabs-voice-assistant.git
cd elevenlabs-voice-assistant
```

2. Install required dependencies:
```bash
pip install elevenlabs elevenlabs[pyaudio] python-dotenv
```

3. Create a `.env` file in the project root with your credentials:
```env
AGENT_ID=your_agent_id_here
API_KEY=your_api_key_here
```

**Important**: Your API key must have the `convai_write` permission enabled. Generate a new API key with Conversational AI permissions from your [ElevenLabs API settings](https://elevenlabs.io/app/settings/api-keys).

## Usage

Run the voice assistant:
```bash
python voice_assistant.py
```

The assistant will start listening. Simply speak naturally, and it will respond. 

To exit the conversation, press `Ctrl+C`.

## Configuration

The assistant can be customized by modifying the conversation configuration in `voice_assistant.py`:

- **user_name**: Personalize responses with your name
- **schedule**: Provide context like your calendar
- **prompt**: Customize the assistant's personality and behavior
- **first_message**: Set the initial greeting

## Troubleshooting

### Authentication Errors
- Ensure your `.env` file is named correctly (with a dot prefix)
- Verify your API key has Conversational AI permissions
- Don't use quotes around values in the `.env` file

### Audio Issues
- Make sure your microphone is properly connected and configured
- Check that PyAudio is installed correctly: `pip install elevenlabs[pyaudio]`

## Credits

Based on work by Alexandre Sajus

## License

MIT
