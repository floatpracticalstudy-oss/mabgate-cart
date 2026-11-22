# Mabgate Cart — browser multiplayer prototype

An original, cartoon-inspired **Leeds/Mabgate street-circuit** racing prototype with a shared cinematic chase-camera screen, QR-code lobby and up to eight smartphone controllers.

## Publish online (Render example)
1. Upload this folder to a GitHub repository.
2. Create a new **Web Service** on Render using that repository.
3. Set Build Command: `npm install` and Start Command: `npm start`.
4. Open the resulting HTTPS address on the host screen, click **Host a Race**, and show the QR code to players.
5. Players scan the code and join with their phones. The host starts the race.

You can also test locally with Node 18+: `npm install && npm start`, then visit `http://localhost:3000`.

## Important prototype limitations
- The Mabgate circuit is **artistically inspired**, not a geographically exact reconstruction. Building geometry and university facade are illustrative placeholders, **not generated from Google Street View or Google Images**.
- The shared screen uses one rotating third-person chase camera and a minimap, **not eight independent split-screen views**.
- Sessions are private via unguessable links and not listed publicly. Anyone possessing the link can join before the lobby is locked; this is **not identity verification**.
- The host must stay connected. Session state is held in server memory; restarts reset races.
- Requires a running WebSocket-capable web host for internet multiplayer. Static-only hosts won't work.
- Cars have arcade handling, track boundaries slow them, and boost charges during driving.
