<p align="center">
  
  ![Orengefox For Marble](assets/social-preview.png)

<p align="center">

  <img src="https://img.shields.io/badge/OrangeFox-Recovery-FF6E1E?style=for-the-badge&logo=android&logoColor=white" />
  <img src="https://img.shields.io/badge/Device-marble%20%7C%20marblein-blue?style=for-the-badge" />
  <img src="https://img.shields.io/badge/License-Apache%202.0-green?style=for-the-badge" />
</p>

<h1 align="center">OrangeFox Recovery — For Marble</h1>
<p align="center">
<b>OrangeFox Recovery Project (OFRP)</b> device tree for <b>Redmi Note 12 Turbo</b> (<code>marble</code>) & <b>POCO F5</b> (<code>marblein</code>)
</p>

---

## 📖 About

This repository contains the device tree used to build **OrangeFox Recovery** for the following Xiaomi devices:

| Market Name | Codename |
| --- | --- |
| Redmi Note 12 Turbo | `marble` |
| POCO F5 | `marblein` |

This device tree is based on **[Ctapchuk/android_device_xiaomi_marble-OFRP](https://github.com/Ctapchuk/android_device_xiaomi_marble-OFRP)**.

## ✨ Features

- Modern, easy-to-use theme
- ZIP, image, and OTA flashing support
- Built-in file manager, terminal, and aFTP
- Full partition backup/restore support
- Data decryption support (format data-friendly)
- MTP, ADB sideload, and ADB shell

## 📥 Installation

1. Download the built OrangeFox image or zip
2. Flash Orengefox.zip in Recovery
3. Boot into fastboot mode: `adb reboot bootloader`
4. Flash it to the boot/recovery partition:
   ```bash
   fastboot flash recovery orangefox-marble.img
   ```
5. Reboot into recovery to verify:
   ```bash
   fastboot reboot recovery
   ```

> ⚠️ Make sure the bootloader is unlocked before flashing.

## 📂 Main Structure

```
device/xiaomi/marble/
├── prebuilt/
├── recovery/root/
├── security/
├── AndroidProducts.mk
├── BoardConfig.mk
├── device.mk
├── fox_marble.mk
├── twrp_marble.mk
├── recovery.fstab
├── vendor.prop
└── vendorsetup.sh
```

## 🙏 Credits & Source

- **OrangeFox Recovery Project** — https://orangefox.tech
- Base device tree: [Ctapchuk/android_device_xiaomi_marble-OFRP](https://github.com/Ctapchuk/android_device_xiaomi_marble-OFRP)
- The TWRP/OFRP community for Xiaomi `marble` & `marblein` devices

## ⚠️ Disclaimer

Flashing a custom recovery may void your device warranty and can cause bootloops or bricking if not done correctly. Use at your own risk — the author/contributors of this repository are not responsible for any damage to your device.

## 📄 License

Distributed under the **Apache License 2.0**, following the upstream OrangeFox/TWRP/AOSP licensing.
