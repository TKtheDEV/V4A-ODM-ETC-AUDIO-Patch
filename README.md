# ViPER4Android QSSI Patch Module

This is a universal patch module for [ViPER4Android FX](https://github.com/WSTxda/ViperFX-RE-Releases) designed for devices using Qualcomm's audio configuration system (QSSI). It automatically injects the required audio effect entries so the V4A driver can be detected correctly.

## Features

- Automatically detects and targets `/odm/etc/audio/sku_*qssi*/audio_effects.xml`
- Injects missing `viper4android_fx` effect and `libv4a_re.so` library references
- Fully dynamic: backs up and bind-mounts the patched file at boot
- Compatible with **Apatch** and **Magisk** (**KernelSU** hasnt been tested)

## Requirements

- Rooted device
- ViPER4Android FX RE installed (use [RE releases here](https://github.com/WSTxda/ViPERFX_RE/releases/latest))
- Driver file must exist at `/vendor/lib64/soundfx/libv4a_re.so`

## Installation

1. Flash Viper4Android and press the "action" button to download and install the App, then flash this patch.
2. Reboot your device.
3. Disable Dolby/Xiaomi sound enhancements in settings
4. Give ViPER4Android FX root access
5. Open ViPER4Android FX.
6. If it doesn't work immediately, enable **Legacy Mode** in settings (you can try disabling it afterwards).

## Troubleshooting
- If your device doesn’t use a `*_qssi` SKU directory, the patch won’t apply. Feel free to expand this patch and send a Pull Request!

## Credits

- ViPER4Android FX RE by [WSTxda](https://github.com/WSTxda)
