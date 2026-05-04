# OneAI Pro - Desktop App Setup

## Installation & Setup

### Prerequisites
- **Node.js** (v14+) - [Download](https://nodejs.org/)
- **npm** (comes with Node)

### Quick Start

1. **Install dependencies:**
   ```bash
   npm install
   ```

2. **Run the app in development:**
   ```bash
   npm start
   ```

3. **Build for your platform:**
   ```bash
   # macOS
   npm run build:mac

   # Windows
   npm run build:win

   # Linux
   npm run build:linux

   # All platforms
   npm run build
   ```

## File Structure

```
OneAI-Pro/
├── electron/
│   ├── main.js          # Electron main process
│   └── preload.js       # Security layer for IPC
├── src/
│   └── OneAI_Pro-2.html # Your chat interface
├── assets/              # Icons for installers
├── package.json         # App configuration
└── README.md           # This file
```

## Features

✅ **Cross-Platform** - Works on Windows, macOS, and Linux
✅ **Standalone** - No need to host on a server
✅ **Voice Enabled** - Full microphone support (unlike file://)
✅ **Persistent Storage** - localStorage works perfectly
✅ **Native App** - Feels like a real desktop application
✅ **Auto-Updater Ready** - Can be configured for updates

## Building Installers

After running `npm run build`, installers will be in the `dist/` folder:

- **macOS**: `.dmg` (installer) or `.zip` (portable)
- **Windows**: `.exe` (installer) or portable `.exe`
- **Linux**: `.AppImage` or `.deb` (installer)

## Development Tips

- Press `Ctrl+Shift+I` (or `Cmd+Shift+I` on Mac) to open DevTools
- Hot-reload is available - save files and they'll update
- Check `electron/main.js` for window configuration

## Troubleshooting

| Issue | Solution |
|-------|----------|
| "Cannot find module 'electron'" | Run `npm install` |
| Voice doesn't work | Voice is now enabled in the app (no HTTPS needed) |
| App won't start | Delete `node_modules/` and run `npm install` again |
| Build fails | Ensure you're on the correct platform and Node.js is installed |

## Next Steps

1. Customize the app icon in `assets/`
2. Update the app name/version in `package.json`
3. Build and distribute to users
4. Consider setting up auto-updates with electron-updater

## Support

For Electron issues, see: https://www.electronjs.org/docs
