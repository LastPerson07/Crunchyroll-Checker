<div align="center">

<br>

```
    ╦  ╔═╗╔═╗╔╦╗╔═╗╔═╗╦═╗╔═╗╔═╗╔╗╔
    ║  ╠═╣╚═╗ ║ ╠═╝║╣ ╠╦╝╚═╗║ ║║║║
       ╩═╝╩ ╩╚═╝ ╩ ╩  ╚═╝╩╚═╚═╝╚═╝╝╚╝ 07
  
    
```

### Crunchyroll Checker V3

**High-Performance Desktop Account Verifier with Proxy Rotation**

<br>

[![Python](https://img.shields.io/badge/Python-3.10%2B-blue?style=for-the-badge&logo=python&logoColor=white)](https://python.org)
[![UI](https://img.shields.io/badge/UI-CustomTkinter-5c6bc0?style=for-the-badge)](https://github.com/TomSchimansky/CustomTkinter)
[![TLS](https://img.shields.io/badge/TLS-curl__cffi-00bcd4?style=for-the-badge)](https://github.com/yifeikong/curl_cffi)
[![License](https://img.shields.io/badge/License-Educational-e040fb?style=for-the-badge)](#-disclaimer)
[![Telegram](https://img.shields.io/badge/Telegram-THE%20UPDATED%20GUYS-26A5E4?style=for-the-badge&logo=telegram&logoColor=white)](https://t.me/THEUPDATEDGUYS)

<br>

> Presented by **[THE UPDATED GUYS 😎](https://t.me/THEUPDATEDGUYS)**

---

<p align="center">
  <a href="https://ibb.co/rGpPkS3C"><img src="https://i.ibb.co/rGpPkS3C/screenshot1.png" alt="Dashboard" width="47%" /></a>
  &nbsp;&nbsp;
  <a href="https://ibb.co/GvFNCMSL"><img src="https://i.ibb.co/GvFNCMSL/screenshot2.png" alt="Checker" width="47%" /></a>
</p>
<p align="center">
  <a href="https://ibb.co/mFTKmS2j"><img src="https://i.ibb.co/mFTKmS2j/screenshot3.png" alt="Stats" width="47%" /></a>
  &nbsp;&nbsp;
  <a href="https://ibb.co/CjSsjcr"><img src="https://i.ibb.co/CjSsjcr/screenshot4.png" alt="Proxies" width="47%" /></a>
</p>

<br>

</div>

---

## ⚡ Overview

**Crunchyroll Checker V3** is a fully native desktop application — no browser, no terminal window, no web server. It's built entirely in Python with CustomTkinter, giving you a clean dark GUI that opens instantly like any other desktop app.

Under the hood it uses aggressive proxy rotation, automatic dead-proxy ejection, and `curl_cffi` TLS fingerprint impersonation to stay ahead of Cloudflare and rate-limit blocks. Every valid hit is logged to disk and optionally pushed to Discord in real time.

---

## 🚀 Features

| Feature | Details |
|---|---|
| **Native Desktop GUI** | Pure CustomTkinter window — no browser, no Electron, no Flask |
| **Smart Proxy Rotation** | Round-robin pool with automatic dead-proxy removal and pool revival |
| **TLS Impersonation** | `curl_cffi` mimics Chrome / Edge / Safari fingerprints to bypass WAF |
| **Cloudflare Evasion** | CF challenges detected automatically and retried on a fresh proxy |
| **Live Results Feed** | Color-coded hits stream in real time with All / Valid / Premium / Invalid filters |
| **Single & Bulk Mode** | Check one account instantly, or paste thousands or import a `.txt` file |
| **Discord Webhook** | Auto-push every valid hit to Discord with full account details embedded |
| **Advanced Mode** | Toggle extended output: account ID, external ID, phone, maturity, debug JSON |
| **Export** | Save results to `.txt` or `.json` directly from the GUI |
| **Live Stats** | Counters for Checked / Valid / Invalid / Premium / Proxies Alive updating every second |
| **One-Click EXE Build** | Includes `build.bat` — produces a fully standalone `.exe` with no Python needed |

---

## 📦 Installation

### ✅ Getting Started

<br>
<a href="../../releases/latest">
  <img src="https://img.shields.io/badge/Download_EXE-Releases_Page-FF5722?style=for-the-badge&logo=windows&logoColor=white" alt="Download EXE" />
</a>
<br><br>

1. Click the button above to go to the **Releases** page.
2. Download `LastPerson07_Checker.exe`.
3. Double-click to run — a GUI window opens instantly! No Python required.

> **Note:** `list.txt` (your proxies) and `results.txt` (your hits) will be created automatically in the same folder as the `.exe`.

---

## 📋 Requirements

```
customtkinter    — Native dark GUI framework
curl_cffi        — Browser TLS fingerprint impersonation
requests         — Discord webhook delivery
PyJWT            — JWT token decoding (subscription detection)
```

<a href="requirements.txt">
  <img src="https://img.shields.io/badge/View_Requirements.txt-Reference-4CAF50?style=for-the-badge&logo=pep8&logoColor=white" alt="View Requirements" />
</a>

---

## 🖥️ How to Use

### 1 — Load Your Proxies

In the **Proxy Manager** panel, paste proxies in any supported format and click **＋ Add**:

```
1.2.3.4:8080
user:password@5.6.7.8:3128
socks5://9.10.11.12:1080
```

Click **⚡ Test All** to ping every proxy and automatically mark dead ones before you start checking.

---

### 2 — Check Accounts

**Single** tab → type `email:password` and press **Enter** or click **▶ Check Account**

**Bulk** tab → paste your combo list (one `email:password` per line) or click **📂 Import from File** to load a `.txt`. Press **🚀 Start Bulk** to begin. Hit **⏹ Stop** at any time.

---

### 3 — Read the Results

Results appear in the **Live Results** panel as checks complete:

| Badge | Meaning |
|---|---|
| `♛ PREMIUM` | Valid account with an active Crunchyroll Premium subscription |
| `✓ VALID` | Valid credentials, free-tier account |
| `✗ INVALID` | Wrong email or password |
| `⚠ ERROR` | Proxy or network failure during check |

Use the **All / Valid / Premium / Invalid** filter buttons to narrow the view. All valid results are also saved automatically to `results.txt`.

---

### 4 — Export & Discord

- **📥 Export TXT** — plain `email:password` list, valid hits only
- **📥 Export JSON** — full objects with status, username, subscription, timestamp
- **Discord Webhook** — enable in the Settings tab and paste your webhook URL for live hit notifications

---

## ⚙️ Settings

| Option | Description |
|---|---|
| **Advanced Mode** | Adds account ID, external ID, phone number, maturity rating, and raw API debug JSON to each result |
| **Discord Webhook** | Toggle on and paste your webhook URL to receive hit notifications instantly |
| **Delay Between Checks** | Milliseconds to wait between each check request. Default: `2000ms`. Lowering speeds things up but increases ban risk |

---

## 🔄 Proxy Rotation Logic

```
Incoming check request
        │
        ▼
   Pick next proxy (round-robin)
        │
        ├─ PROXY_DEAD   → Mark dead, pick next proxy
        ├─ RATE_LIMITED → Sleep 1s, pick next proxy
        ├─ CLOUDFLARE   → Mark dead, pick next proxy
        ├─ invalid_grant → Return INVALID immediately (no retry)
        └─ HTTP 200      → Return result ✓

• Up to 6 proxy attempts per account before hard failure
• Dead proxies are ejected from the rotation pool automatically
• If ALL proxies are dead, the pool resets and retries from scratch
```

---

## 📁 File Structure

```
📂 Crunchyroll-Checker/
 ├── LastPerson07_Checker.exe ← Main application (Download latest release)
 ├── requirements.txt         ← Dependency references
 ├── list.txt                 ← Your proxy list (auto-created on launch)
 └── results.txt              ← Valid accounts log (auto-created on hits)
```

---

## ❓ FAQ

**My antivirus flags the EXE — is it safe?**
> Yes. Packaged Python executables frequently trigger false positives because they unpack temporary files to execute. It is completely safe.

**Can I run it without proxies?**
> No. The endpoint rate-limits direct IPs very aggressively. You need at least a working proxy pool to get usable throughput.

**What proxy formats are supported?**
> `ip:port`, `user:pass@ip:port`, and `socks5://ip:port`. HTTP and HTTPS proxies both work.

**Where are results saved?**
> Every valid hit is appended to `results.txt` in the same folder as the exe automatically. You can also export manually from the GUI in TXT or JSON format.

**The GUI window doesn't open / crashes on launch?**
> Ensure your antivirus isn't automatically blocking the background process, or try running the application as an Administrator.

---

## 👥 Credits

Built by **[LastPerson07](https://github.com/LastPerson07)**  
Presented by **[THE UPDATED GUYS 😎](https://t.me/THEUPDATEDGUYS)**

Join us on Telegram for updates, new tools, and more:  
**➜ [t.me/THEUPDATEDGUYS](https://t.me/THEUPDATEDGUYS)**

---



<br>

<sub><i>⚠️ Disclaimer: This software is provided strictly for educational and authorized security research purposes only. The author and publisher accept no liability for misuse. Always obtain explicit authorization before testing any account, system, or online service.</i></sub>

<br>

</div>
