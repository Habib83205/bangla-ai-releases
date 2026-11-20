# Security Policy — Bangla AI (বাংলা এআই)

**Maintainer:** Habib Nabil  
**Repository:** `Habib83205/bangla-ai`

---

## Supported Versions

Only the latest published release receives active security patches and silent desktop updates.

| Version | Status |
| :--- | :--- |
| **`BanglaAi v1.4` (Latest)** | ✅ Actively Supported & Receiving Silent Updates |
| `< v1.4` | ⚠️ Please update to the latest version via **Settings → General → Check for updates** |

---

## Built-In Safety Protections

1. **Localhost Binding:** The internal Bangla AI desktop backend binds strictly to `127.0.0.1` and accepts Work Mode automation requests solely from local loopback connections.
2. **Catastrophic Command Blocking:** Destructive OS-level shell patterns (disk formatting, recursive wipes of system drives/directories, registry hive deletion) are blocked unconditionally across all permission levels.
3. **Recycle Bin Protection:** File and folder deletions initiated via Work Mode move items safely to the **Windows Recycle Bin** rather than permanently erasing them.
4. **Secret Isolation:** `.env` files, personal keys, and user credentials are ignored by Git and excluded from compiled `.exe` installer packages.
5. **Context Isolation:** The Electron desktop renderer runs with `contextIsolation: true`, `nodeIntegration: false`, and `sandbox: true`, communicating only through a minimal audited preload bridge.

---

## Reporting a Vulnerability

If you discover a security vulnerability in **Bangla AI**, please report it responsibly instead of opening a public issue:

1. Use GitHub's **Private Vulnerability Reporting** (Security Advisories) in this repository, or reach out directly to **Habib Nabil** via [GitHub (@Habib83205)](https://github.com/Habib83205).
2. Include clear reproduction steps, affected version (`BanglaAi vX.Y`), and potential impact.
3. Confirmed vulnerabilities are prioritized and patched via the **1-Click Silent Auto-Update** release pipeline.
