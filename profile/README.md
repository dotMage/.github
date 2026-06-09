<div align="center">
  <b>dotMage</b> — self-hosted, E2E-encrypted <code>.env</code> secret manager.
  <br>
  <sub>the server never sees your secrets. ever.</sub>
</div>

<br>

**how it works**

your master password derives a key locally. secrets are encrypted on your device with XChaCha20-Poly1305 before touching the network. the server stores only encrypted blobs — it physically cannot read your `.env` files.

<br>

**install**

macOS
```bash
brew install dotMage/dotmage/dotmage
```

Linux
```bash
curl -fsSL -o dmage https://github.com/dotMage/dotmage/releases/latest/download/dmage-linux-x86_64 && chmod +x dmage
```

Windows
```powershell
irm https://raw.githubusercontent.com/dotMage/dotmage/main/install.ps1 | iex
```

**deploy server** (one command)
```bash
curl -fsSL https://raw.githubusercontent.com/dotMage/dotmage-server/main/install.sh | bash
```

<br>

**repos**

| repo | what |
|---|---|
| [**dotmage**](https://github.com/dotMage/dotmage) | CLI tool `dmage` — crypto core, client, binary (Rust) |
| [**dotmage-server**](https://github.com/dotMage/dotmage-server) | API server — encrypted blob storage (Python/FastAPI) |
| [**dotmage-web**](https://github.com/dotMage/dotmage-web) | Admin panel — read-only metadata viewer (React/TS) |
| [**dotmage-spec**](https://github.com/dotMage/dotmage-spec) | Specification, API contract, threat model |

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

<sub>AGPL-3.0 · self-hosted · zero-knowledge</sub>

</div>
