Elevate your community messaging with professional, elegantly formatted announcements. Select a channel, craft your message, and dispatch it with a single, intuitive slash command.

## ✨ Features

- 🎯 **Channel Selector:** Directly pick any text or announcement channel from the Discord client UI.
- 🎨 **Embed Customization:** Supports headlines, multi-line content, and custom hex color codes (e.g., `#FFD700`).
- 🖼️ **Banner Images:** Optionally include a custom image or GIF banner to make your announcements pop.
- 🔐 **Secure Design:** Restricted to server administrators only (via `PermissionFlagsBits.Administrator`).
- ⚡ **Seamless Slash Commands:** No messy prefix prefix commands—all interactions use Discord’s latest built-in interface.

## 🚀 How to Set Up

### 𝟭. Bot Registration

1. Go to the [Discord Developer Portal](https://discord.com/developers/applications).
2. Create a **New Application** and give it a name (e.g., "Broadcast Buddy").
3. Navigate to the **Bot** tab, and generate a **Token**.
4. In the **Privileged Gateway Intents** section, ensure `MESSAGE CONTENT INTENT` is enabled (though slash commands don't strictly require it, it's good practice for advanced bots).
5. Open `.env` and paste your token: `DISCORD_TOKEN=your_token_here`.

### 𝟮. Installation & Running

Ensure you have [Node.js](https://nodejs.org/) installed, then run:

```bash
# Register commands and start the broadcast engine
npm start
```

## 🛠️ Commands

### `/announce`
Send a high-impact announcement to any channel.

- **`target_channel`**: The channel to send to.
- **`headline`**: The bold title for your announcement.
- **`content`**: The message body (supports `\n` for new lines).
- **`color`** *(optional)*: Hex code like `#7289da`.
- **`image_url`** *(optional)*: A direct link to a banner image.

---

*Designed for the Antigravity community by your AI assistant.*
