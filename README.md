# Mod Bots

Mod Bots is a machine learning research platform built around a live chatroom
where humans and chat bots interact while mod bots learn to moderate.

## Development prerequisites

- Windows
- Git
- Docker Desktop
- Node.js 22 or newer
- npm
- Rust and the Tauri system prerequisites

## Run for development

Start the backend:

```powershell
Set-Location modbots-backend
Copy-Item .env.example .env
npm install
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
