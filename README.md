# DeckTap (LAN MVP)

📡 DeckTap is a lightweight local-network remote for controlling presentations.  
Use your phone to wirelessly control PowerPoint, Keynote, PDF slideshows — no app installation needed.

---

## ✨ Features

- 📱 Control slides via your phone browser
- 🌐 Works over local Wi-Fi network
- 🖥 Simulates keyboard arrow keys to navigate slides
- 🚀 Minimal setup: run a local Node.js server and scan a QR code
- 🔒 No internet required, safe and private

---

## 📦 Project Structure
```yaml
decktap/
├── client/            # Computer side agent
│    ├── lan.js        # LAN control
│    ├── cloud.js      # Connect cloud relay server in the future
│    └── config.js
│
├── controller/        # Mobile phone controller web page
│    └── index.html
│
├── server-cloud/      # Cloud server for remote control in the future
│    └── server.js
│
├── README.md
├── LICENSE
├── package.json
└── .gitignore
```
---

## 🔧 Prerequisites

### macOS Permissions
DeckTap uses `@nut-tree/nut-js` to simulate keyboard events. On macOS, you need to grant Accessibility permissions to your terminal:

1. Open **System Settings** > **Privacy & Security** > **Accessibility**
2. Click the lock icon 🔒 to make changes
3. Click the **+** button
4. Select `Terminal.app` (or iTerm, VS Code, etc. depending on what you use)
5. Check the box next to your terminal app

> **Note**: Without these permissions, DeckTap won't be able to control your presentations.

---

## 🚀 Getting Started (LAN Mode)
1. Install dependencies:
   ```bash
   npm install
   ```

2. Grant accessibility permissions (macOS only):
   - Follow the steps in [macOS Permissions](#macos-permissions)
   - Restart your terminal after granting permissions

3. Start the server:
   ```bash
   npm start
   ```

4. Connect with your phone:
   - Connect your phone to the same WiFi network as your computer
   - Open the displayed URL in your phone's browser
   - Start controlling your presentation