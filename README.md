# RoVault

> A Roblox account manager for Windows. Store, organize, and launch multiple accounts from one place.

---

## Features

### Account Management
- **Unlimited accounts** — add accounts via login window, cookie paste, manual entry, or bulk text import
- **One-click launch** — jump into any game from any account instantly with Place ID and optional Job ID
- **Multi-account launch** — select multiple accounts and launch them all into the same server sequentially
- **Account groups** — organize accounts with custom group tags and filter by group
- **Drag-and-drop reordering** — arrange accounts in any order you want
- **2FA / TOTP support** — stores and autofills authenticator codes
- **Notes** — attach and edit notes per account from the right-click menu
- **Right-click context menu** — copy credentials, set group, view notes, open account utilities
- **Search & filter** — real-time search by username, group, or "2fa"; filter by status (All, Online, Offline, Locked, Signed Out, In Game)
- **Bulk actions** — Ctrl+click multi-select for batch launch, group assignment, or deletion
- **Cookie validation** — automatic signed-in / signed-out detection via Roblox API
- **Import methods** — login window, cookie paste, bulk TXT file, and JSON format
- **Account cards** — color-coded avatars with initials, status badges, login count, last login time, online/in-game indicators, and hover action buttons

### Account Utilities
- **View & edit** — email, password, display name, phone number for any account
- **Change password** — updates on Roblox and auto-saves the new cookie
- **Change email & phone** — direct Roblox API calls from the app
- **Set display name** — with rate-limit detection (7-day cooldown warning)
- **Age group display** — computed from birthdate with phone verification badge
- **Social networks** — shows linked Facebook, Twitter, YouTube, Twitch, Guilded with visibility badges (Everyone, No One, etc.)
- **Email & phone verification status** — green checkmark if verified, orange "Not Verified" badge if not

### Launch & Game
- **Three launch methods** — Normal (bootstrapper or direct), UWP (Microsoft Store), and Multi-Instance mode
- **Bootstrapper auto-detection** — detects Bloxstrap, Fishstrap, Froststrap, and other bootstrappers automatically
- **Multi-instance** — launch multiple Roblox clients simultaneously
- **Region selector** — auto-detect or manually pick US East, US West, EU West, Asia Pacific, or South America
- **Game name resolver** — fetches game name from Place ID automatically
- **Save game places** — save up to 20 favorite Place IDs for one-click join
- **Browser play** — open accounts in a full Roblox browser window with in-page game detection and "Save game to RoVault?" prompts
- **Friend-join interception** — join friends from the in-app browser and it launches through RoVault automatically
- **Protocol handler** — registered as default handler for `roblox://` and `roblox-player://` URLs
- **Smart launch queue** — detects when each game client is ready before launching the next account, preventing collisions

### Presence & Status Tracking
- **Real-time online status** — polls Roblox Presence API to show who's online, in-game, in Studio, or offline
- **In-game detection** — shows game name and Place ID for accounts currently playing
- **Bloxstrap RPC** — integrates with Bloxstrap/Froststrap for rich presence data
- **Activity log** — timestamped notification history with unread badge counter
- **Session tracking** — per-account login and game session history stored locally with timestamps and game info
- **Open accounts panel** — shows currently open Roblox browser windows with close buttons

### Tracker Tab
- **Overview** — account statistics and summary dashboard
- **Sessions** — login and game session timeline per account with duration tracking
- **Compare** — side-by-side comparison of up to 3 accounts
- **Playtime analytics** — most-played games ranking, day-of-week login patterns, session duration analysis

### Macro System
- **4 trigger types** — No Repeat (one-shot), Repeat While Holding, Toggle (start/stop), Sequence (step-through per press)
- **8 action types** — key press, key combo, type text, mouse click, mouse move, mouse path, delay, launch game
- **DirectInput simulation** — works in games that use raw input / DirectInput
- **Mouse path recording** — record and replay smooth mouse movements with interpolation
- **Global hotkeys** — bind any Ctrl/Alt/Shift + key combo, plus Mouse4/Mouse5 side buttons
- **Macro recorder** — record keyboard and mouse input in real-time with global key state monitoring; auto-generates macro steps
- **Instant execution** — macros fire immediately on hotkey press with no startup delay
- **Interruptible** — toggle macros can stop instantly when you press the hotkey again
- **Folder organization** — organize macros into named folders
- **My Apps** — save and manage macro application collections

### Account Generator
- **Automated account creation** — full signup flow with birthday, username, password, and gender selection
- **Smart username generation** — multiple generation modes with automatic retry for finding valid names
- **CAPTCHA handling** — detects CAPTCHAs and prompts you to solve them manually in a visible browser window
- **Proxy support** — HTTP and SOCKS5 proxies with authentication
- **Live progress** — streams each generated account to the UI as it completes
- **Cookie extraction** — automatically captures session cookie from successful signups

### Auto-Login (Import TXT)
- **Bulk login** — import and log into multiple accounts sequentially with visible browser windows (not headless)
- **CAPTCHA handling** — detects CAPTCHAs and opens a visible window for manual solving
- **2FA detection** — prompts for 2FA code entry when required
- **Proxy routing** — assign proxies per login attempt with round-robin assignment
- **Progress tracking** — real-time per-account result logs with success/failure status and step-by-step log output
- **Proxy presets** — loopback presets or custom proxy input

### Remote Desktop (RDP)
- **RDP Wrapper integration** — one-click install with step-by-step progress display
- **Update INI** — fetch latest community-maintained INI to stay compatible with new Windows builds
- **Start Service** — start TermService directly from the app with UAC elevation; shows running state
- **Status dashboard** — real-time cards for RDP Wrapper, TermService, RDP enabled/disabled, RDP Plus availability, Windows build number, and listening port
- **Favorites** — saved RDP connections with slot-based loopback IPs, user profile selector, window title, custom resolution, and options (No Drives, No Sound, No Wallpaper, Console, Fullscreen, Keyboard Hook)
- **User Profiles** — create and delete local Windows users with auto-assignment to Administrators and Remote Desktop Users groups
- **RDP Plus profiles** — auto-creates RDP Plus saved profiles for new users so connections work immediately
- **RDP Plus or mstsc** — launches via RDP Plus if available, falls back to built-in mstsc.exe
- **Open Folder** — quick access to the RDP Wrapper installation directory

### Discord Rich Presence
- **Activity display** — shows game name and "Playing as [username]" in Discord
- **Auto-reconnect** — reconnects automatically if Discord restarts
- **Bloxstrap RPC** — integrates with Bloxstrap/Froststrap for in-game presence
- **Auto-update** — updates presence when switching games or accounts
- **Toggle on/off** — enable or disable from Settings

### Themes & Customization
- **8 preset themes** — Crimson, Ocean, Violet, Gold, Forest, Rose, Neon, Slate
- **Custom theme editor** — pick any three accent colors with live preview; create new or edit existing themes
- **Save & load themes** — create, rename, update, and delete unlimited custom themes
- **13 background animations** — Particles, Matrix, Waves, Nebula, Aurora, Rain, Stars, Fireflies, Void, Lava Lamp, Snow, Hypnotic, or None
- **Themed splash screens** — startup and goodbye splash screens with audio, matching your active theme colors
- **App entry animations** — after splash, the app scales in with blur, sidebar slides from left, content rises from below

### Backup & Import
- **Export vault** — save all accounts to an encrypted .rvault file with SHA-256 checksum
- **Import vault** — restore from .rvault or .json backup with checksum validation
- **Import TXT** — bulk import from text files with auto-format detection and proxy support
- **Data location** — vault path and macro storage path shown in Settings for easy manual backup

### News Tab
- **RoVault changelog** — version history with detailed feature descriptions, bug fixes, and release dates
- **Roblox DevForum feed** — live RSS feed from the Roblox Blog and DevForum with category badges, view/reply stats, and LATEST indicator
- **Built-in webview** — read DevForum posts without leaving the app, with "Open in browser" button

### Aria Tooltips
- **Contextual help** — hover info icons on non-obvious UI elements for Aria-branded explanations
- **Covers** — Place ID, Job ID, Settings toggles, Launch Method, Multi-Instance Mode, Backup & Restore, RDP Slot/Profile, Macro types, Status filters, 2FA badges

### API Key Manager
- **Per-service storage** — save API keys for external services
- **Show/hide toggle** — visibility control for each stored key
- **Encrypted storage** — keys stored in the encrypted vault alongside account data

### Settings
- **Desktop notifications** — toggle native Windows notifications
- **Discord Rich Presence** — toggle Discord activity display
- **Debug mode** — show console log output with copy buttons
- **Launch method** — switch between Normal, UWP, and Multi-Instance
- **Multi-Instance info panel** — expandable explainer for how multi-instance mode works under the hood
- **Master password** — encrypt and decrypt account fields with a session password
- **RDP Plus path** — configure custom RDP client path via file browser

### Credits
- **Creator profile** — M12D8 / W2F4U with links
- **Beta testers** — individual cards with unique accent colors
- **Built With** — tech stack display (Electron, React, Node.js, JavaScript, PowerShell, C#, Python, HTML, CSS, JSON, SQL)
- **The Story** — evolution from "Roblox Helper" (2024) to RoVault

### Quality of Life
- **System tray** — minimize to tray, stays ready in the background
- **Auto-lock** — vault locks itself after inactivity
- **Single instance** — prevents multiple copies from running; second launch restores the existing window
- **Animated splash screens** — themed startup and goodbye screens with audio and progress bar
- **Auto-updater** — checks for updates and notifies when a new version is ready
- **Desktop notifications** — native Windows notifications for key events
- **Roblox already running detection** — warns on startup if Roblox is already open
- **WebAuthn/passkey suppression** — auto-dismisses Windows Security passkey dialogs during login
- **Custom title bar** — frameless borderless window with minimize, maximize, close-to-tray, and quit buttons plus draggable area

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

All data is stored **locally** in `%APPDATA%\rovault\`. Nothing is sent to any server. Your accounts never leave your device.

To wipe all data, delete the `rovault` folder.

---

## Security

| Layer | Details |
|---|---|
| Vault encryption | AES-256-GCM with per-installation unique key |
| Key derivation | PBKDF2-SHA256 |
| Per-field encryption | Each sensitive field encrypted individually |
| IPC boundary | Whitelisted channels only — no raw IPC access in renderer |
| Renderer | Node integration disabled, context isolation enabled |
| Content Security Policy | Restrictive CSP enforced on all windows |
| HTTPS enforcement | All external fetches require HTTPS |
| Permission handlers | All Chromium permission requests denied by default |
| DevTools | Blocked in production builds |
| Source code | Obfuscated, no source maps in release |
| Input sanitization | Path traversal protection, shell injection guards |

---

## Disclaimer

RoVault is an independent project not affiliated with or endorsed by Roblox Corporation. Use in accordance with Roblox's Terms of Service.
