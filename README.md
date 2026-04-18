# NanoClaw — Unraid Community Applications Template

Unraid CA template for **NanoClaw**, a lightweight secure personal AI agent for Unraid.

## Installation

1. In Unraid, go to **Apps** and search for **NanoClaw**
2. Or add this template repository to your CA settings:
   `https://raw.githubusercontent.com/bitcryptic-gw/unraid-nanoclaw/main/NanoClaw.xml`

## Requirements

* Anthropic API key from **console.anthropic.com**
* **Telegram** bot token from **@BotFather**, and/or a **Matrix** homeserver account (e.g. self-hosted Synapse)
* Docker socket access (required for agent container isolation)

## Messaging Channels

NanoClaw supports multiple chat backends. You can use one or both:

**Telegram** — trigger the agent via your bot using the configured trigger word. Set `TELEGRAM_BOT_TOKEN` from @BotFather. After starting the container, send `/chatid` to your bot and note the returned ID, then run the registration command (see the [NanoClaw README](https://github.com/qwibitai/nanoclaw)).

**Matrix (E2EE)** — connect NanoClaw to a Matrix room on any homeserver with full end-to-end encryption. Configure `MATRIX_HOMESERVER_URL`, `MATRIX_BOT_USER_ID`, and `MATRIX_ACCESS_TOKEN`. The bot password (`MATRIX_BOT_PASSWORD`) is only needed once to bootstrap cross-signing keys and can be removed afterwards.

## First Run

1. Start the container and check logs to confirm it connects successfully
2. **Telegram:** send `/chatid` to your bot, note the returned ID, then run the registration command
3. **Matrix:** ensure your bot account exists on the homeserver, set the three Matrix env vars, and start the container — it will join configured rooms automatically

Full setup instructions are in the [NanoClaw README](https://github.com/qwibitai/nanoclaw).

## Optional Integrations

NanoClaw supports a growing list of self-hosted integrations configurable via environment variables:

* **Tailscale** — join your tailnet for secure private access
* **Home Assistant** — smart home control and automation
* **Vikunja** — task and project management
* **Ollama / LiteLLM** — local model inference
* **Paperclip** — AI agent orchestration
* **UnraidClaw** — manage your Unraid servers directly from chat

See the template XML for full details on each integration's environment variables.

## Docker Image

`bitcryptic/nanoclaw:latest` — built from [bitcryptic-gw/nanoclaw](https://github.com/bitcryptic-gw/nanoclaw)

## Support

* [NanoClaw project](https://github.com/qwibitai/nanoclaw)
* [Unraid forums support thread](https://forums.unraid.net/topic/197773-support-nanoclaw-lightweight-secure-ai-agent-for-unraid/)
