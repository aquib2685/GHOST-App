# GHOST App

**Speak freely. Vanish completely.**

An anonymous messaging application where all posts auto-delete at midnight. No logs. No traces. No memory.

## Features

- 🔐 **Anonymous**: Generate unique ghost identities for each session
- ⏰ **Auto-Delete**: All messages vanish at midnight every day
- 💬 **Real-time**: Live feed of all community messages
- 🎨 **Minimal Design**: Clean, distraction-free interface
- 📱 **Responsive**: Works on all devices

## Getting Started

### Prerequisites

- Node.js (v14+)
- npm or yarn

### Installation

1. Clone the repository:
```bash
git clone https://github.com/aquib2685/GHOST-App.git
cd GHOST-App
```

2. Install dependencies:
```bash
npm install
```

3. Start the development server:
```bash
npm start
```

4. Open [http://localhost:3000](http://localhost:3000) in your browser

## Development

- `npm start` - Run dev server
- `npm run build` - Build for production
- `npm test` - Run tests

## How It Works

1. **Generate Identity**: Click "Generate My Identity" on first visit
2. **Write Messages**: Type your anonymous message (max 400 characters)
3. **Share**: Send to the shared feed instantly
4. **Auto-Delete**: All messages disappear at midnight (00:00)

## Tech Stack

- React 18
- CSS3
- Local Storage API

## Deployment

See [DEPLOYMENT.md](./DEPLOYMENT.md) for hosting instructions.

## License

MIT License - Feel free to use this project for any purpose.

## Privacy

- No backend servers store your data
- All messages stored locally in browser
- Messages deleted at midnight daily
- Your identity is never logged or tracked

---

**Remember**: This is meant for temporary, anonymous conversation. Don't rely on this for sensitive information.
