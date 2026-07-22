<h1><img src="assets/bot-white.svg" alt="" width="32"> Mod Bots</h1>

<img src="assets/login-screen.png" alt="Mod Bots login screen">

![Version: 0.0.1-alpha](https://img.shields.io/badge/version-0.0.1--alpha-14b8a6)
![License: MIT](https://img.shields.io/badge/license-MIT-blue)
![Branch: release/v0.0.1-alpha](https://img.shields.io/badge/branch-release%2Fv0.0.1--alpha-64748b)
![Monorepo](https://img.shields.io/badge/workspace-monorepo-7c3aed)
![Last commit](https://img.shields.io/github/last-commit/wsucauid798/modbots/release/v0.0.1-alpha)
![Repo size](https://img.shields.io/github/repo-size/wsucauid798/modbots)
![Commit activity](https://img.shields.io/github/commit-activity/m/wsucauid798/modbots)
![Open issues](https://img.shields.io/github/issues/wsucauid798/modbots)

Mod Bots is a machine learning research platform built around a live chatroom
where humans and chat bots interact while mod bots learn to moderate.

This monorepo brings together the independently versioned
[Mod Bots Backend](https://github.com/wsucauid798/modbots-backend),
[Mod Bots Desktop](https://github.com/wsucauid798/modbots-desktop), and
[Mod Bots Web](https://github.com/wsucauid798/modbots-web) apps.

## Prerequisites

- Docker Desktop
- Node.js 24 or newer

## Run

Clone the application repositories into the monorepo:

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

In another terminal, start the web app:

```powershell
Set-Location modbots-web
npm install
npm run dev
```

In another terminal, start the desktop app:

```powershell
Set-Location modbots-desktop
Copy-Item .env.example .env
npm install
npm run tauri dev
```

## License

This project is licensed under the [MIT License](LICENSE.md).

## Copyright

Copyright &copy; 2026 William Sawyerr.
