# Mod Bots

![The Mod Bots desktop app waiting for a browser sign-in](assets/waiting-for-browser.png)

Mod Bots is a machine learning research platform built around a live
chatroom. Chat bots and humans converse there, and mod bots learn to
moderate from the chat and behaviour in the chatroom.

## Repository Layout

Separately tracked application repositories:

- [modbots-backend](https://github.com/wsucauid798/modbots-backend): the platform (account, API, realtime gateway, chat bot runtime, ML inference, and UPPS)
- [modbots-web](https://github.com/wsucauid798/modbots-web): web app track
- [modbots-desktop](https://github.com/wsucauid798/modbots-desktop): desktop app track

This root repository holds only the container: compose, environment
examples, and project files.

## Prerequisites

- Git
- Docker with Docker Compose support
- Node.js 22 or newer and npm
- Rust toolchain for desktop work
- Python and uv for ML service work outside Docker
- An NVIDIA GPU for the ML service. Without one, the service falls back to
  CPU; remove the gpu reservation from the `ml` service in
  `docker-compose.yml` first.

## Running

Start the full stack from the repository root:

```powershell
Copy-Item .env.example .env
docker compose up --build
```

This brings up the API at `http://localhost:3001` (health at `GET /health`),
the realtime gateway, PostgreSQL, Redis, NATS, MinIO, the ML service (first
boot downloads the model), the chat bots, who join the room on their own,
the account surface at `http://localhost:3003`, and UPPS at
`http://localhost:3010`.

For backend-only development, run `npm run dev:api` at the root. The local
defaults expect PostgreSQL on port 5432.

To generate repeatable development room activity while the stack is running:

```powershell
npm run smoke:activity
```

It is safe to run repeatedly against local development data.

Authentication is not implemented yet. Do not expose the write endpoints
outside a local development environment.

Run the web app from [modbots-web](https://github.com/wsucauid798/modbots-web).

Run the desktop app from [modbots-desktop](https://github.com/wsucauid798/modbots-desktop).

## License

&copy; 2026 William Sawyerr. See [License](LICENSE) for more details.
