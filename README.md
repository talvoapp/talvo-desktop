# Talvo Desktop

**Medical Supplies & Pharmaceuticals Management System**

Talvo Desktop is a comprehensive ERP system designed for pharmacies, medical stores, and medical supplies companies. It provides full support for **multi-branch operations**, **remote access via Cloudflare Tunnel**, and **multi-tenant architecture**.

[![Version](https://img.shields.io/badge/version-1.0.2-blue.svg)](https://github.com/talvoapp/talvo-desktop/releases)
[![Platform](https://img.shields.io/badge/platform-Windows%207%2B-lightgrey.svg)](https://github.com/talvoapp/talvo-desktop)
[![License](https://img.shields.io/badge/license-Proprietary-red.svg)](https://github.com/talvoapp/talvo-desktop)

---

## 📥 Download

Download the latest version from the [Releases page](https://github.com/talvoapp/talvo-desktop/releases).

| Version | File | Size | Release Date |
|---------|------|------|--------------|
| **v1.0.2** | `Talvo_Setup_1.0.2.exe` | 197 MB | October 2026 |

---

## ✨ Features

<details>
<summary><b>Core Features (Click to expand)</b></summary>

- 📊 **Dashboard** — Real-time business insights
- 💰 **Sales Management** — Invoices, returns, and customer accounts
- 🛒 **Purchases Management** — Purchase orders, invoices, and supplier management
- 📦 **Inventory Management** — Stock tracking, batches, and expiration dates
- 👥 **Customer Management** — Accounts, discounts, and profit reports
- 🏢 **Supplier Management** — Purchase history and price comparison
- 👨‍💼 **Employee Management** — Salaries, bonuses, and attendance
- 📈 **Reports** — Sales, purchases, profit, and inventory reports
- 🔒 **Multi-Tenant** — Support for multiple companies

</details>

<details>
<summary><b>Advanced Features (Click to expand)</b></summary>

- 🌐 **Multi-Branch Support** — Local and remote branches
- ☁️ **Cloudflare Tunnel** — Remote access from anywhere
- 🔄 **Automatic Backups** — Every 60 minutes
- 🔐 **Role-Based Access Control** — 222 permissions across 8 roles
- 🌍 **Arabic Support** — Full RTL support
- 🔒 **VPN Support (Nebula)** — Private network support

</details>

---

## 🛠️ Technology Stack

| Layer | Technology |
|-------|------------|
| **Frontend** | PyQt5 |
| **Backend** | Flask |
| **Database** | SQLite |
| **Packaging** | Nuitka |
| **Installer** | Inno Setup |
| **Remote Access** | Cloudflare Tunnel |
| **VPN** | Nebula |

---

## 💻 System Requirements

<details>
<summary><b>Minimum Requirements (Click to expand)</b></summary>

| Component | Requirement |
|-----------|-------------|
| **OS** | Windows 7 SP1 or later (64-bit) |
| **RAM** | 4 GB |
| **Storage** | 500 MB free space |
| **CPU** | Dual-core 2.0 GHz |
| **Internet** | Required for cloud sync |
| **Display** | 1280×720 or higher |

</details>

<details>
<summary><b>Recommended Requirements (Click to expand)</b></summary>

| Component | Requirement |
|-----------|-------------|
| **OS** | Windows 10/11 (64-bit) |
| **RAM** | 8 GB or more |
| **Storage** | 1 GB free space |
| **CPU** | Quad-core 2.5 GHz |
| **Internet** | Broadband (5 Mbps+) |
| **Display** | 1920×1080 or higher |

</details>

---

## 📦 Installation

<details>
<summary><b>Step-by-Step Installation (Click to expand)</b></summary>

### 1. Download
Download `Talvo_Setup_1.0.2.exe` from the [Releases page](https://github.com/talvoapp/talvo-desktop/releases).

### 2. Run Installer
Double-click `Talvo_Setup_1.0.2.exe` to start the installation.

### 3. Follow the Wizard
- Accept the license agreement
- Choose installation folder (default: `C:\Program Files\Talvo`)
- Select additional tasks (see below)

### 4. Additional Tasks

| Task | Master Device | Branch Device |
|------|---------------|---------------|
| **Install Talvo Server Service** | ✅ **YES** | ❌ No |
| **Install Cloudflare Tunnel Service** | ✅ **YES** | ❌ No |

> **⚠️ Important:**
> - **Master Device**: Only ONE device. Install both services.
> - **Branch Device**: Multiple devices. Don't install any services.

### 5. Complete Installation
Click **Install** and wait 2–5 minutes.

### 6. First Launch
- Open `Talvo.exe` from Start Menu or Desktop
- Enter your credentials:
  - **Master**: `license_key` + `username` + `password`
  - **Branch**: `branch_code` + `username` + `password`

</details>

---

## 🏗️ Architecture

<details>
<summary><b>System Architecture (Click to expand)</b></summary>

```
┌─────────────────────────────────────────────┐
│              Cloud (Vercel)                 │
│  ┌────────────────────────────────────────┐ │
│  │  API + Tenant Registry                 │ │
│  └────────────────────────────────────────┘ │
└─────────────────────────────────────────────┘
              ▲                    ▲
              │                    │
┌─────────────┴──────────┐  ┌──────┴──────────┐
│   Master Device        │  │  Branch Device  │
│  ┌──────────────────┐  │  │                 │
│  │ Talvo Server     │  │  │  Talvo.exe      │
│  │ (Port 5000)      │  │  │  (Remote)       │
│  └──────────────────┘  │  │                 │
│  ┌──────────────────┐  │  └─────────────────┘
│  │ Cloudflare Tunnel│  │         ▲
│  └──────────────────┘  │         │
└────────────────────────┘         │
         ▲                         │
         └─────────────────────────┘
              Via Cloudflare
```

</details>

---

## 🔐 Verification

After downloading, verify the file integrity:

```cmd
certutil -hashfile Talvo_Setup_1.0.2.exe SHA256
```

| File | SHA256 |
|------|--------|
| `Talvo_Setup_1.0.2.exe` | `4781bb1011857e90fb57ed94a0de875f93e2841e86d662f620ebd17bf159f4b9` |

**Expected output:**
```
SHA256 hash of Talvo_Setup_1.0.2.exe:
4781bb1011857e90fb57ed94a0de875f93e2841e86d662f620ebd17bf159f4b9
CertUtil: -hashfile command completed successfully.
```

---

## 📄 License

**Proprietary** — © 2026 Talvo. All rights reserved.

This software is proprietary and confidential. Unauthorized copying, distribution, or modification is strictly prohibited.

---

## 🆘 Support

| Channel | Details |
|---------|---------|
| **Email** | info@tech-company.com |
| **Website** | https://talvo.com |
| **Issues** | [GitHub Issues](https://github.com/talvoapp/talvo-desktop/issues) |
| **Releases** | [GitHub Releases](https://github.com/talvoapp/talvo-desktop/releases) |

---

## 🙏 Contributing

This is a **private** repository. Contributions are by invitation only.

For inquiries, contact: info@tech-company.com

---

**Made with ❤️ by the Talvo Team**
