# WhatsApp Voice Chat Bot

A Node.js client for [WhatsApp Web](https://github.com/pedroslopez/whatsapp-web.js) that combines conversational AI with optional **voice replies**. Users can interact in text or voice; the bot can transcribe incoming audio, call an LLM (OpenAI-compatible flow), and synthesize spoken responses via **ElevenLabs** (with optional integrations for other providers).

## Features

- WhatsApp Web session (QR login) via `whatsapp-web.js`
- Text and voice message handling with configurable interaction modes
- Speech-to-text and text-to-speech pipeline for vocal replies
- Allowlist-based access control for authorized phone numbers

## Prerequisites

- Node.js 18+ recommended
- Active accounts/API keys for the providers you enable (e.g. OpenAI, ElevenLabs)
- Environment variables as required by your deployment (see `src/` modules)

## Setup

1. Clone the repository and install dependencies (add a `package.json` if your copy does not include one; typical dependencies include `whatsapp-web.js`, `qrcode-terminal`, and your chosen SDKs).

   ```bash
   npm install
   ```

2. Configure environment variables for API keys, phone allowlists, and provider-specific settings. The entry point is `src/index.js`.

3. Start the bot:

   ```bash
   node src/index.js
   ```

4. Scan the QR code in the terminal with WhatsApp on your phone to authenticate.

## Demo

[Watch the demo video](https://drive.google.com/file/d/1tpEpcjmpuEhdz8GTcRWQxOfMIRZoqENs/view?usp=sharing)

## Project layout

| Path | Role |
|------|------|
| `src/index.js` | Session setup, message routing, and command handling |
| `src/openai/` | LLM and transcription helpers |
| `src/elevenlabs/` | Text-to-speech integration |
| `src/utils/` | Shared utilities |

## Disclaimer

This software interacts with third-party APIs and WhatsApp’s unofficial Web client. Use in compliance with WhatsApp’s terms of service and applicable laws. Not affiliated with Meta.

## License

See the repository license file if present.
