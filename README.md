<h1><img src="assets/bot-white.svg" alt="" width="32"> Mod Bots</h1>

<img src="assets/login-screen.png" alt="Mod Bots login screen">

![Monorepo](https://img.shields.io/badge/workspace-monorepo-7c3aed)
![Version: 0.0.1-alpha](https://img.shields.io/badge/version-0.0.1--alpha-14b8a6)
![Branch: release/v0.0.1-alpha](https://img.shields.io/badge/branch-release%2Fv0.0.1--alpha-64748b)
![License: MIT](https://img.shields.io/badge/license-MIT-blue)
![Last commit](https://img.shields.io/github/last-commit/wsucauid798/modbots/release/v0.0.1-alpha)

This is the project container for [Mod Bots](https://modbots.ai), which is a platform for teaching cognitive learning agents how to moderate real-time human to human, agent to agent and human to agent communication. The project container is a monorepo that brings together the related [Mod Bots Backend](https://github.com/wsucauid798/modbots-backend),
[Mod Bots Desktop](https://github.com/wsucauid798/modbots-desktop) and
[Mod Bots Web](https://github.com/wsucauid798/modbots-web) applications.

## Prerequisites

- Docker Desktop
- Node.js 24 or newer

## Run

Clone the source for each of the related applications into the monorepo:

```powershell
git clone https://github.com/wsucauid798/modbots-backend.git
git clone https://github.com/wsucauid798/modbots-desktop.git
git clone https://github.com/wsucauid798/modbots-web.git
```

Start the backend:

```powershell
Set-Location modbots-backend
Copy-Item .env.example .env
docker desktop enable model-runner
docker compose up --build
```

Start the desktop app:

```powershell
Set-Location modbots-desktop
Copy-Item .env.example .env
npm install
npm run tauri dev
```

Start the web app:

```powershell
Set-Location modbots-web
Copy-Item .env.example .env
npm install
npm run dev
```

## License

Mod Bots is licensed under the [MIT License](LICENSE.md).

## Copyright

Copyright &copy; 2026 William Sawyerr.
