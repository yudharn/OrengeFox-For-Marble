<p align="center">
  
  ![OrangeFox For Marble](assets/social-preview.png)

<p align="center">

  <img src="https://img.shields.io/badge/OrangeFox-Recovery-FF6E1E?style=for-the-badge&logo=android&logoColor=white" />
  <img src="https://img.shields.io/badge/Device-marble-blue?style=for-the-badge" />
  <img src="https://img.shields.io/badge/License-Apache%202.0-green?style=for-the-badge" />
</p>

<h1 align="center">OrangeFox Recovery — For Marble</h1>
<p align="center">
GitHub Actions build for <b>OrangeFox Recovery Project (OFRP)</b> on <b>POCO F5</b> / <b>Redmi Note 12 Turbo</b> (<code>marble</code>)
</p>

---

## 📖 About

This repository **does not contain a device tree**. It contains a GitHub Actions workflow
(`.github/workflows/OrengeFox.yml`) that syncs the OrangeFox `fox_12.1` sources, clones the device tree
at build time, builds the recovery, and publishes the result as a GitHub Release.

| Market Name | Codename |
| --- | --- |
| POCO F5 | `marble` |
| Redmi Note 12 Turbo | `marble` |

The device tree used by default is **[Ctapchuk/android_device_xiaomi_marble-OFRP](https://github.com/Ctapchuk/android_device_xiaomi_marble-OFRP)** (branch `fox_12.1`).

## ✨ Features

- Modern, easy-to-use theme
- ZIP, image, and OTA flashing support
- Built-in file manager, terminal, and aFTP
- Full partition backup/restore support
- Data decryption support (format data-friendly)
- MTP, ADB sideload, and ADB shell

## 🔨 How to build

1. Open the **Actions** tab → **Recovery OFOX Build (fox_12.1) — marble** → **Run workflow**.
2. Keep the defaults, or change the inputs (device tree URL/branch, maintainer name, patch version).
3. Wait for the job to finish (about 1 hour). The recovery `.zip` appears under **Releases**.

Only the repository owner can start the workflow. If a build fails, the full `build.log` is attached to the run as an artifact for 7 days.

## 📥 Installation

Each release contains one file: the flashable **OrangeFox recovery `.zip`**, named like
`OrangeFox-R12.0_<patch>-Unofficial-marble.zip`.

1. Download the `.zip` from **Releases**.
2. Boot into a working custom recovery (for example an older OrangeFox or TWRP build for `marble`).
3. Flash the `.zip`.
4. Reboot back into recovery to verify.

> ℹ️ The release has no `.img`, so the zip needs an already working custom recovery to be flashed from.
> ⚠️ Make sure the bootloader is unlocked before flashing.

## 📂 Repository Structure

```
.
├── .github/
│   ├── dependabot.yml
│   └── workflows/
│       └── OrengeFox.yml
├── assets/
│   └── social-preview.png
└── README.md
```

## 🙏 Credits & Source

- **OrangeFox Recovery Project** — https://orangefox.tech
- Device tree: [Ctapchuk/android_device_xiaomi_marble-OFRP](https://github.com/Ctapchuk/android_device_xiaomi_marble-OFRP)
- The TWRP/OFRP community for Xiaomi `marble` devices

## ⚠️ Disclaimer

Flashing a custom recovery may void your device warranty and can cause bootloops or bricking if not done correctly. Use at your own risk — the author/contributors of this repository are not responsible for any damage to your device.

## 📄 License

Distributed under the **Apache License 2.0**, following the upstream OrangeFox/TWRP/AOSP licensing.
