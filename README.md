<h1 align="center">LineageOS for Google Pixel 8a (akita)</h1>

<div align="center">

<p><i>Official repository for LineageOS 24.0 (Android 17) OTA updates and release distribution for the Google Pixel 8a.</i></p>

[![LineageOS](https://img.shields.io/badge/LineageOS-24.0-167C80?style=for-the-badge&logo=lineageos&logoColor=white)](https://lineageos.org/)
[![Android](https://img.shields.io/badge/Android-17-3DDC84?style=for-the-badge&logo=android&logoColor=white)](https://www.android.com/)
[![Latest Release](https://img.shields.io/github/v/release/rhythmcreative/lineageos-akita-ota?color=blue&style=for-the-badge)](https://github.com/rhythmcreative/lineageos-akita-ota/releases/latest)

</div>

---

## 📡 Canales de Actualización / Release Channels

| Canal | Rama Git | Estado | Última Versión | Enlace de Descarga |
| :--- | :--- | :--- | :--- | :--- |
| 🟢 **Stable** | [`main`](https://github.com/rhythmcreative/lineageos-akita-ota/tree/main) | *En preparación* | — | Próximamente |
| 🟡 **Beta** | [`beta`](https://github.com/rhythmcreative/lineageos-akita-ota/tree/beta) | **Activo** | `2026-09-07` | [Descargar Release](https://github.com/rhythmcreative/lineageos-akita-ota/releases/tag/akita-2026-09-07) |
| 🔴 **Alpha** | [`alpha`](https://github.com/rhythmcreative/lineageos-akita-ota/tree/alpha) | *Promovido a Beta* | — | *(Consolidado en Beta)* |

---

## 📱 Dispositivo

| Propiedad | Valor |
| :--- | :--- |
| **Dispositivo** | Google Pixel 8a |
| **Nombre en clave** | `akita` |
| **Versión ROM** | LineageOS 24.0 (Android 17) |
| **Arquitectura** | ARM64 (`arm64-v8a`) |
| **Firma** | Clave privada oficial (OTA verificable) |

---

## 🔄 Cómo actualizar

1. **Desde la aplicación Actualizaciones (OTA)**:
   * Ajustes > Sistema > Actualizaciones.
   * En los ajustes del actualizador, selecciona el canal deseado (**Beta** o **Estable**).
   * Pulsa en **Buscar actualizaciones** y presiona **Descargar e instalar**.

2. **Vía Recovery / ADB Sideload**:
   * Descarga el paquete firmado desde [Releases](https://github.com/rhythmcreative/lineageos-akita-ota/releases).
   * Reinicia en modo recovery: `adb reboot sideload`
   * Instala el paquete: `adb sideload lineage-24.0-*.zip`

---

<div align="center">
<sub>Compilado y mantenido con ❤️ por rhythmcreative</sub>
</div>
