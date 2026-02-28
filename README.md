# openclaw-zalo-bot

OpenClaw Zalo channel plugin (Bot API) — patched fork.

## Fixes

- **`photo_url` field mapping**: Correctly parses the Zalo Bot API's `photo_url` field for image messages (the original plugin incorrectly expected `photo`)
- **Image + Caption handling**: When a user sends both an image and text caption, both are now correctly forwarded to the AI agent (the original plugin dropped the image when caption text was present)

## Installation

```bash
# On your Linux server:
npm install -g github:vuminhtuanhvtc/openclaw-zalo-bot

# Then restart the gateway:
openclaw gateway restart
```

## License

MIT
