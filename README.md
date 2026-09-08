<h1 align="center">LineageOS 24.0 for Google Pixel 8a (akita)</h1>

<div align="center">

<p><i>Official repository for LineageOS 24.0 (Android 17) OTA updates, fastboot images, and release distribution for the Google Pixel 8a.</i></p>

[![LineageOS](https://img.shields.io/badge/LineageOS-24.0-167C80?style=for-the-badge&logo=lineageos&logoColor=white)](https://lineageos.org/)
[![Android](https://img.shields.io/badge/Android-17-3DDC84?style=for-the-badge&logo=android&logoColor=white)](https://www.android.com/)
[![Latest Release](https://img.shields.io/github/v/release/rhythmcreative/lineageos-akita-ota?color=blue&style=for-the-badge)](https://github.com/rhythmcreative/lineageos-akita-ota/releases/latest)

</div>

---

## 📡 Canales de Actualización / Release Channels

| Canal | Rama Git | Estado | Enlace de Descarga |
| :--- | :--- | :--- | :--- |
| 🟢 **Stable** | [`main`](https://github.com/rhythmcreative/lineageos-akita-ota/tree/main) | *En preparación* | Próximamente |
| 🟡 **Beta** | [`beta`](https://github.com/rhythmcreative/lineageos-akita-ota/tree/beta) | **Activo** | [Descargar Releases](https://github.com/rhythmcreative/lineageos-akita-ota/releases) |
| 🔴 **Alpha** | [`alpha`](https://github.com/rhythmcreative/lineageos-akita-ota/tree/alpha) | *Promovido a Beta* | *(Consolidado en Beta)* |

---

## 📱 Especificaciones del Dispositivo

| Propiedad | Valor |
| :--- | :--- |
| **Dispositivo** | Google Pixel 8a |
| **Nombre en clave** | `akita` |
| **SoC** | Google Tensor G3 (`zuma`) |
| **Versión ROM** | LineageOS 24.0 (Android 17) |
| **Arquitectura** | ARM64 (`arm64-v8a`) |
| **Firma** | Clave privada oficial RSA 4096 (OTA verificable & AVB 2.0) |

---

## 🚀 Guía de Instalación Limpia (Primera Instalación)

Sigue estos pasos para una instalación limpia y estable a la primera en el Pixel 8a:

### Requisitos Previos
1. Bootloader desbloqueado (`fastboot flashing unlock`).
2. Última versión de **Android Platform Tools** (`adb` y `fastboot`).
3. Descargar los archivos del [último Release](https://github.com/rhythmcreative/lineageos-akita-ota/releases):
   - `boot.img`
   - `dtbo.img`
   - `init_boot.img`
   - `vendor_boot.img`
   - `vendor_kernel_boot.img`
   - `pkmd.bin` *(opcional, para rebloquear con Verified Boot)*
   - `lineage-24.0-*-UNOFFICIAL-akita-signed.zip`

---

### Paso 1: Flashear Particiones de Arranque (Fastboot Mode)
Conecta el dispositivo en modo Fastboot (`adb reboot bootloader` o manteniendo **Volumen Abajo + Encendido**):

```bash
fastboot flash boot boot.img
fastboot flash dtbo dtbo.img
fastboot flash init_boot init_boot.img
fastboot flash vendor_boot vendor_boot.img
fastboot flash vendor_kernel_boot vendor_kernel_boot.img
```

---

### Paso 2 (Opcional): Clave AVB para Verified Boot con Bootloader Rebloqueado
Si deseas rebloquear el bootloader manteniendo la seguridad de Verified Boot:

```bash
fastboot erase avb_custom_key
fastboot flash avb_custom_key pkmd.bin
```

---

### Paso 3: Entrar a Recovery y Formatear Datos
1. En la pantalla de Fastboot, usa las teclas de volumen para seleccionar **Recovery Mode** y pulsa el botón **Encendido**.
2. En LineageOS Recovery:
   - Selecciona **Factory Reset** > **Format data / factory reset**.
   - Confirma el formateo.

---

### Paso 4: Instalar LineageOS 24.0
1. En el menú principal de Recovery, selecciona **Apply update** > **Apply from ADB**.
2. Desde la terminal de tu PC:
   ```bash
   adb sideload lineage-24.0-*-UNOFFICIAL-akita-signed.zip
   ```
3. Espera a que complete al 100% (o 47% con `Step 2/2 Complete`).

---

### Paso 5: Reiniciar
- Si NO vas a rebloquear el bootloader: Selecciona **Reboot system now**.
- Si flasheaste `pkmd.bin` y quieres rebloquear: Selecciona **Reboot to bootloader** y ejecuta en el PC:
  ```bash
  fastboot flashing lock
  ```
  Confirma en la pantalla del dispositivo y éste arrancará de forma segura con Verified Boot activo (pantalla de aviso amarilla de custom key).

---

## 🔄 Actualización (Dirty Flash / OTA)

### 1. Desde la aplicación Actualizaciones (OTA)
- **Ajustes** > **Sistema** > **Actualizaciones**.
- Pulsa **Buscar actualizaciones**, selecciona la última versión beta o estable y presiona **Descargar e instalar**.

### 2. Vía Recovery / ADB Sideload
- Descarga el archivo `lineage-24.0-*-UNOFFICIAL-akita-signed.zip`.
- Reinicia en recovery: `adb reboot sideload`
- Instala la actualización sin borrar datos:
  ```bash
  adb sideload lineage-24.0-*-UNOFFICIAL-akita-signed.zip
  ```
- Reinicia el dispositivo.

---

<div align="center">
<sub>Compilado y mantenido con ❤️ por rhythmcreative</sub>
</div>
