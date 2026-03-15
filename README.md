# NanoClaw — Unraid Community Applications Template

Unraid CA template for [NanoClaw](https://github.com/qwibitai/nanoclaw), a lightweight secure personal AI agent.

## Installation

1. In Unraid, go to **Apps** and search for **NanoClaw**
2. Or add this template repository to your CA settings:
   `https://raw.githubusercontent.com/bitcryptic-gw/unraid-nanoclaw/main/NanoClaw.xml`

## Requirements

- Anthropic API key from [console.anthropic.com](https://console.anthropic.com) OR Claude Pro/Max OAuth token
- Telegram bot token from [@BotFather](https://t.me/BotFather)

## First Run

After starting the container:
1. Open Telegram and send `/chatid` to your bot
2. Note the chat ID returned
3. Run the registration command (see [NanoClaw README](https://github.com/qwibitai/nanoclaw))

## Docker Image

`bitcryptic/nanoclaw:latest` — built from [bitcryptic-gw/nanoclaw](https://github.com/bitcryptic-gw/nanoclaw)

## Support

- [NanoClaw project](https://github.com/qwibitai/nanoclaw)
- [Unraid forums thread](https://forums.unraid.net) (coming soon)
