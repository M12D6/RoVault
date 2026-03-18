# RoVault

> A Roblox account manager for Windows. Store, organize, and launch multiple accounts from one place.

---

## Features

- **Multi-account vault** — add and manage unlimited Roblox accounts
- **One-click launch** — jump into any game from any account instantly
- **Account groups** — organize accounts into folders
- **2FA / TOTP support** — stores and autofills authenticator codes
- **Macro recorder** — record and replay keyboard & mouse sequences with hotkey triggers
- **Discord Rich Presence** — shows your activity in Discord
- **Proxy support** — assign proxies per account
- **Backup & restore** — export your vault to a file and import it anywhere
- **Auto-lock** — vault locks itself after inactivity
- **System tray** — minimizes to tray and stays ready in the background
- **Themes** — multiple built-in themes

---

## Download

Get the latest installer from the [Releases](../../releases) page.

| File | Description |
|---|---|
| `RoVault-Setup-x.x.x-x64.exe` | 64-bit installer (recommended) |
| `RoVault-Setup-x.x.x-ia32.exe` | 32-bit installer |
| `RoVault-Portable-x.x.x.exe` | Portable — runs without installing |

---

## Building from Source

**Requirements:** Node.js 18+, Windows 10/11

```bash
git clone https://github.com/your-username/rovault.git
cd rovault
npm install

# Development (hot reload)
npm run electron:dev

# Build installer
npm run electron:build
```

Output is in `dist/`.

---

## Data & Privacy

All data is stored **locally** on your machine:

```
C:\Users\<you>\AppData\Roaming\rovault\rovault-data.json
```

Nothing is sent to any server. Your accounts never leave your device.

To wipe all data, delete that file.

---

## Security

| Layer | Details |
|---|---|
| Vault encryption | AES-256-GCM |
| Key derivation | PBKDF2-SHA256, 310,000 iterations |
| IPC boundary | `contextBridge` with whitelisted channels only |
| Renderer | `nodeIntegration: false`, `contextIsolation: true` |
| DevTools | Blocked in production builds |
| Source code | Obfuscated, no source maps in release |

---

## Disclaimer

RoVault is an independent project not affiliated with or endorsed by Roblox Corporation. Use in accordance with Roblox's Terms of Service.
