<h1><img src="assets/bot-white.svg" alt="" width="32"> Mod Bots</h1>

<img src="assets/login-screen.png" alt="Mod Bots login screen">

![Version: 0.0.1-alpha](https://img.shields.io/badge/version-0.0.1--alpha-14b8a6)
![License: MIT](https://img.shields.io/badge/license-MIT-blue)
![Branch: release/v0.0.1-alpha](https://img.shields.io/badge/branch-release%2Fv0.0.1--alpha-64748b)
[![Backend CI](https://github.com/wsucauid798/modbots-backend/actions/workflows/ci.yml/badge.svg?branch=release/v0.0.1-alpha)](https://github.com/wsucauid798/modbots-backend/actions/workflows/ci.yml)
[![Backend Deploy](https://github.com/wsucauid798/modbots-backend/actions/workflows/deploy-backend.yml/badge.svg)](https://github.com/wsucauid798/modbots-backend/actions/workflows/deploy-backend.yml)
[![Desktop CI](https://github.com/wsucauid798/modbots-desktop/actions/workflows/ci.yml/badge.svg?branch=release/v0.0.1-alpha)](https://github.com/wsucauid798/modbots-desktop/actions/workflows/ci.yml)
[![Web CI](https://github.com/wsucauid798/modbots-web/actions/workflows/ci.yml/badge.svg?branch=main)](https://github.com/wsucauid798/modbots-web/actions/workflows/ci.yml)
![Docker](https://img.shields.io/badge/backend-Docker-2496ED?logo=docker&logoColor=white)
![Tauri](https://img.shields.io/badge/desktop-Tauri-24C8DB?logo=tauri&logoColor=white)
![Next.js](https://img.shields.io/badge/web-Next.js-000000?logo=nextdotjs&logoColor=white)

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
