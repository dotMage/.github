<div align="center">
  <b>dotMage</b> — self-hosted, E2E-encrypted <code>.env</code> secret manager.
  <br>
  <sub>the server never sees your secrets. ever.</sub>
</div>

<br>

**how it works**

your master password derives a key locally. secrets are encrypted on your device with XChaCha20-Poly1305 before touching the network. the server stores only encrypted blobs — it physically cannot read your `.env` files. and not just `.env`: any config file syncs with its name encrypted too.

**solo or team** — one product, two modes. solo is a team of one; invite a colleague and each member gets their own master password over the shared vault, with server-enforced roles, per-person audit and one-command offboarding (`dmage user rm` chains into a key rotation).

<br>

**install the CLI**

macOS
```bash
brew install dotMage/dotmage/dotmage
```

Linux
```bash
curl -fsSL -o dmage https://github.com/dotMage/dotmage/releases/latest/download/dmage-linux-$(uname -m) && chmod +x dmage
```

Windows
```powershell
irm https://raw.githubusercontent.com/dotMage/dotmage/main/install.ps1 | iex
```

upgrading later is built in: `dmage upgrade` (sha256-verified self-update).

**use from Python** — same E2E crypto, as a library

```bash
pip install dotmage
```

**deploy a server** (one command)

```bash
# solo — personal vault
curl -fsSL https://raw.githubusercontent.com/dotMage/server/main/install.sh | bash

# team — same installer, one flag
curl -fsSL https://raw.githubusercontent.com/dotMage/server/main/install.sh | DOTMAGE_MODE=team bash
```

<br>

**repos**

| repo | what |
|---|---|
| [**dotmage**](https://github.com/dotMage/dotmage) | CLI tool `dmage` — crypto core, client, binary (Rust) |
| [**server**](https://github.com/dotMage/server) | API server — encrypted blob storage (Python/FastAPI) |
| [**web**](https://github.com/dotMage/web) | Admin panel — read-only metadata viewer (React/TS) |
| [**dotmage-python**](https://github.com/dotMage/dotmage-python) | Python SDK — typed client + client-side crypto (`pip install dotmage`) |

**more**: [docs](https://dotmage.github.io/docs/) · [vs Infisical / Vaultwarden / sops / Doppler](https://dotmage.github.io/docs/#compare) · [blog & release notes](https://dotmage.github.io/blog/)

<br>

<div align="center">

![Rust](https://img.shields.io/badge/rust-000000?style=flat-square&logo=rust&logoColor=white)
![Python](https://img.shields.io/badge/python-3776AB?style=flat-square&logo=python&logoColor=white)
![React](https://img.shields.io/badge/react-61DAFB?style=flat-square&logo=react&logoColor=black)
![TypeScript](https://img.shields.io/badge/typescript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![FastAPI](https://img.shields.io/badge/fastapi-009688?style=flat-square&logo=fastapi&logoColor=white)
![SQLite](https://img.shields.io/badge/sqlite-003B57?style=flat-square&logo=sqlite&logoColor=white)
![Docker](https://img.shields.io/badge/docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/github%20actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)

<br>

<sub>AGPL-3.0 · self-hosted · zero-knowledge · solo & team</sub>

</div>
