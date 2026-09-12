<div align="center">

# SkidTechnologies

### *Complete Python Port of Pterodactyl Panel & Wings with Rootless Runtimes*

[![GitHub followers](https://img.shields.io/github/followers/SkidTechnologies?label=Follow&style=for-the-badge&logo=github&color=30363d)](https://github.com/SkidTechnologies)
[![License](https://img.shields.io/badge/License-MIT-blue.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)
[![Python Version](https://img.shields.io/badge/Python-3.10%2B-blue?style=for-the-badge&logo=python&logoColor=white)](https://python.org)
[![Port of Pterodactyl](https://img.shields.io/badge/Port%20of-Pterodactyl-007acc?style=for-the-badge&logo=pterodactyl&logoColor=white)](https://pterodactyl.io)

<p align="center">
  <b>SkidTechnologies</b> is an open-source initiative providing a <b>full Python port of the Pterodactyl ecosystem</b>. We bring complete 1:1 compatibility with Pterodactyl's egg system, API endpoints, and control plane protocols, built from the ground up in high-performance Python with user-space rootless runtimes that run anywhere.
</p>

---

</div>

## 🌌 The Ecosystem

```
┌─────────────────────────────────────────────────────────────┐
│                       SkidTechnologies                      │
│                 (Pterodactyl Python Port)                   │
└──────────────────────────────┬──────────────────────────────┘
                               │
            ┌──────────────────┴──────────────────┐
            ▼                                     ▼
   ┌─────────────────┐                   ┌─────────────────┐
   │     pypanel     │ ───────────────►  │     pywings     │
   │ Pterodactyl     │      API / WS     │ Pterodactyl     │
   │ Panel Port      │                   │ Wings Port      │
   └─────────────────┘                   └─────────────────┘
```

### 🖥️ [pypanel](https://github.com/SkidTechnologies/pypanel)
> **Direct Python port of the Pterodactyl Panel.**

- **1:1 Pterodactyl Panel Port:** Fully compatible with Pterodactyl's database schema, server models, nodes, egg configurations, and user permissions.
- **Pure Python Architecture:** Eliminates complex PHP runtime dependencies and background queue setups in favor of fast, native asynchronous Python.
- **Direct Node Orchestration:** Communicates seamlessly with both `pywings` nodes and standard Wings daemons via REST API and WebSockets.
- **Egg & Variable System:** Native support for standard Pterodactyl egg exports, environment variables, startup commands, and configuration file matchers.
- **Real-Time Control:** Live CPU, memory, disk, and network stats with an interactive, reactive web console.

---

### 🦅 [pywings](https://github.com/SkidTechnologies/pywings)
> **Direct Python port of Pterodactyl Wings daemon powered by rootless udocker.**

- **1:1 Pterodactyl Wings Port:** Complete drop-in replacement for the Go-based Wings daemon, implementing identical API endpoints, WebSocket streams, and backup protocols.
- **Powered by udocker (Zero Root / Zero Sudo):** Runs containerized game servers 100% in user-space using `udocker` and PRoot. No Docker daemon socket (`/var/run/docker.sock`) or `sudo` required.
- **Universal Portability:** Deployable on unprivileged VPS, shared hosting, Android/Termux, or restricted enterprise environments where traditional Docker cannot run.
- **Full Wings Protocol:** Live console streaming, egg startup done-line matchers, automated installer scripts with Panel status reporting, backup archives, node transfers, and integrated SFTP server (port `2022`).

---

## 🛠️ Technology Stack

<div align="center">

| Component | Technology | Purpose |
| :--- | :--- | :--- |
| **Foundation** | Pterodactyl Port | 1:1 compatibility with Pterodactyl protocols & egg ecosystem |
| **Backend Core** | Python 3.10+ | Clean, fast, and maintainable implementation |
| **Node Engine** | `udocker` / PRoot | Unprivileged, user-space container execution |
| **Communication** | REST API & WebSockets | Low-latency state synchronization & live terminal streams |
| **File Transfer** | Paramiko / Native SFTP | Integrated SFTP on port `2022` with Panel authentication |
| **Security** | JWT & Granular Grants | Pterodactyl-compliant token authorization and scoped permissions |

</div>

---

## 💡 Why SkidTechnologies?

- 🦖 **Full Pterodactyl Compatibility:** 100% compatible with existing eggs, variables, and protocols from the Pterodactyl community.
- 🔒 **No Root Daemon Exposure:** Standard Wings requires root access to the host Docker daemon. `pywings` runs entirely in user-space via `udocker`.
- 🪶 **Minimal Idle Footprint:** Optimized Python services with low memory footprint, ideal for small VPS, edge nodes, and cost-efficient infrastructure.
- 📦 **Plug-and-Play Interoperability:** Use `pypanel` with `pywings`, or pair either component with official Pterodactyl services.

---

<div align="center">

<sub>Built with passion by <b>SkidTechnologies</b>. Proudly ported from the incredible open-source foundation of the <b>Pterodactyl Project</b>.</sub>

</div>
