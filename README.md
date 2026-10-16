# GatherFrame — Watch together, wherever 🍿

GatherFrame is a real-time watch-party web app where friends can create a private room, sync YouTube playback, chat, react, build a shared queue, and vote on what to watch next. This version has a fresh visual identity and a redesigned responsive interface.

## Run locally
Requirements: Node.js 18+ and npm.

```bash
npm install
npm start
```
Open http://localhost:3000. Create a room, then open the invite link in another browser/incognito window with a different nickname to test multi-user behavior.

## Features
- Private rooms with shareable room codes and invite links
- Host-led synchronized YouTube playback with guest drift correction
- Live chat and emoji reactions
- Searchable movie suggestions, genre filters, shared playlist, and custom YouTube videos
- Live polls and host transfer
- Responsive layout for laptop and mobile
- `/health` endpoint for a basic server status check

## Notes
This is an MVP/demo. Rooms are stored in memory and are cleared when the server restarts. YouTube embedding permissions vary by video. For a production release, add persistence, authentication, rate limiting, moderation, and stronger room authorization.

## Structure
- `server.js` — Express + Socket.IO backend
- `public/index.html` — page structure
- `public/style.css` — GatherFrame visual system
- `public/app.js` — client-side interactions and synchronized playback
