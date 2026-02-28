# @openclaw/zalo-bot

OpenClaw Zalo channel plugin (Bot API) — patched fork.

## AI Install Metadata
- Plugin id: zalo_bot
- Channel id: zalo_bot
- Package name: @openclaw/zalo-bot

## Fixes

- **`photo_url` field mapping**: Correctly parses the Zalo Bot API's `photo_url` field for image messages
- **Image + Caption handling**: When a user sends both an image and text caption, both are now correctly forwarded to the AI agent

## Install (local checkout)

```bash
# Clone the repo
git clone https://github.com/vuminhtuanhvtc/openclaw-zalo-bot.git
cd openclaw-zalo-bot

# Install dependencies
npm install

# Register with OpenClaw
openclaw plugins install .
```

Restart Gateway after installation.

## Quick Start

Add channel config to `openclaw.json`:

```json
{
  "channels": {
    "zalo_bot": {
      "enabled": true,
      "token": "YOUR_ZALO_BOT_TOKEN",
      "webhookUrl": "https://your-domain.com/zalo_bot-webhook",
      "webhookSecret": "your-webhook-secret",
      "dmPolicy": "open"
    }
  }
}
```

Then restart:

```bash
openclaw gateway restart
```

## License

MIT
