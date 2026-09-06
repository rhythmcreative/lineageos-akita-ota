<h1 align="center">LineageOS for Pixel 8a</h1>

<div align="center">

<p><i>OTA update support for the Google Pixel 8a (akita), providing the latest available LineageOS builds.</i></p>

[![LineageOS](https://img.shields.io/badge/LineageOS-167C80?style=for-the-badge&logo=lineageos&logoColor=white)](https://lineageos.org/)
[![Android](https://img.shields.io/badge/Android-3DDC84?style=for-the-badge&logo=android&logoColor=white)](https://www.android.com/)
[![OTA](https://img.shields.io/badge/OTA-Update-167C80?style=for-the-badge&logo=android&logoColor=white)](#)
[![Active](https://img.shields.io/badge/Status-Active-2EA44F?style=for-the-badge)](#)

</div>

## About

This repository contains the OTA metadata required to provide update information for the Google Pixel 8a (`akita`).

The repository is intentionally minimal and contains the update configuration used by the LineageOS updater.

## Device

| Property      | Value           |
| ------------- | --------------- |
| Device        | Google Pixel 8a |
| Codename      | `akita`         |
| ROM           | LineageOS       |
| Update method | OTA             |
| Architecture  | ARM64           |

## Repository Structure

```text
.
└── akita.json
```

## OTA

The `akita.json` file contains the information required by the updater to detect and provide available OTA builds for the device.

> **Note:** This repository only provides OTA metadata. The actual LineageOS builds are hosted separately.

## Changes

### Akita 2026-09-06 (LineageOS 24.0)
- Excluida la aplicación Search (`QuickSearchBox`) del sistema.
- Activado PIN Scrambling (desorden de teclado numérico) en la pantalla de bloqueo y en el desbloqueo de SIM.
- Integrados ajustes avanzados de seguridad y protección contra exploits (`ExploitProtectionSettings`).
- Añadido parche de recuperación de secreto FRP para flasheos limpios (`PersistentDataBlockService`).
- Sincronización con las últimas fuentes upstream de LineageOS 24.0 (Android 16 / Baklava).
- Build firmada con clave privada propia y soporte para bloqueo de bootloader (AVB).

### Akita 2026-09-05 (LineageOS 24.0)
- Build inicial de LineageOS 24.0 para Pixel 8a (`akita`).
- Integración oficial de MindTheGapps para Android 16.
- Configuración de URI de actualizador OTA propio.

## Disclaimer

This is an unofficial project and is not affiliated with or endorsed by the LineageOS project or Google.
<div align="center">

<p>Made with ❤️ from rhythmcreative.</p>

</div>
