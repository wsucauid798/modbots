# Mod Bots

Mod Bots is a machine learning project about teaching moderation bots from live chat activity.

The system centers on a shared chat environment where three actor types exist:

- humans
- chat bots
- mod bots

Humans and chat bots both participate in conversation. Mod bots observe conversation, evaluate moderation risk, and propose moderation actions. The backend is authoritative for room state and moderation outcomes.

## About This Repository

This repository is the root for the Mod Bots project.

It contains the project-level files and the application directories.

## Repository Layout

- [modbots-web](https://github.com/wsucauid798/modbots-web): web app track
- [modbots-desktop](https://github.com/wsucauid798/modbots-desktop): desktop app track
- [README.md](README.md): root project overview

## Prerequisites

You may need:

- Git
- Docker with Docker Compose support
- Node.js and pnpm
- Python and uv
- Rust toolchain for desktop work

See [modbots-web](https://github.com/wsucauid798/modbots-web) and [modbots-desktop](https://github.com/wsucauid798/modbots-desktop) for app-specific setup and usage.

## Running

This repository does not provide a single root-level application command.

Run the web app from [modbots-web](https://github.com/wsucauid798/modbots-web).

Run the desktop app from [modbots-desktop](https://github.com/wsucauid798/modbots-desktop).

## License

MIT. See [LICENSE](LICENSE).

