# Jonathan 8.16 OFF — Jonathan 8.16 OFF

Starter project for a French personal AI assistant with a provider-neutral server, web UI, browser voice dictation/speech, and local conversation history.


## What is real in this package
- Responsive mobile web interface.
- Express server and `/api/status` health endpoint.
- `/api/chat` route using a chat-completions-compatible endpoint configured via environment variables.
- Local chat history in the browser (localStorage).
- Browser speech recognition (availability varies by browser) and text-to-speech.
- Provider adapter is intentionally generic: no AI provider is connected until the server secrets are configured.

## Run (requires a computer or cloud development environment)
1. Install Node.js 18+.
2. In this folder, run `npm install`.
3. Copy `.env.example` to `.env` and set `AI_API_URL`, `AI_API_KEY`, `AI_MODEL`.
4. Run `npm start`.
5. Open the local server URL shown in terminal.

Deploy the folder to a Node hosting service that supports persistent environment variables. Do not put API secrets in browser files or commit `.env`.

## Security and limitations
- This is a starter project, not a deployed public service.
- The AI endpoint must support the chat-completions request shape used in `server.js` or be adapted.
- Browser speech recognition requires a compatible browser and typically an internet connection; speech synthesis depends on device/browser voices.
- Conversation history is stored locally in the browser, not encrypted and not synced to a cloud database.
- API credentials and billing must be managed by a parent/guardian for a minor.
