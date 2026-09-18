# English Speaking

A free, beginner-friendly English speaking practice app. Practice conversation, pronunciation repetition, level assessment, and confidence-building exercises directly in the browser.

## Free-first promise
English Speaking is designed to be usable without payment, an account, or an API key. The browser version uses device speech features and local progress storage.

Optional server AI integrations may be enabled by a maintainer, but they are not required for learners.

## Features

- Beginner, Intermediate, and Advanced placement flow
- Speaking and repeat-after-me practice
- Daily 10-minute practice plan
- Daily conversation, travel, interview, and workplace topics
- Ava, Leo, Smriti, and Alex voice personalities
- Speed and accent settings
- Local progress and streak interface
- Export and delete local data
- PWA/offline shell
- Optional AI feedback and neural text-to-speech backend

## Run locally

Requirements: Node.js 18 or newer.

```bash
node server.js
```

Open `http://localhost:3000`.

No environment variables are required for free mode. Optional server AI configuration is documented in `.env.example`.

## Privacy

The free mode stores progress in the browser and does not intentionally save audio recordings. Read [PRIVACY_POLICY.md](PRIVACY_POLICY.md) before deploying publicly. Replace the contact placeholder before release.

## Project status

The browser/PWA prototype is working. Android packaging, production pronunciation scoring, cloud accounts, and notifications require separate integration and physical-device testing. See [PLAY_STORE_RELEASE.md](PLAY_STORE_RELEASE.md).

## Contributing

Issues and pull requests are welcome. Please do not commit API keys, user recordings, passwords, or private data.

## License

MIT License. See [LICENSE](LICENSE).
