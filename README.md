# Windows11-Unattended-Installation


This project contains an `autounattend.xml` configuration for automating the Windows installation process with custom settings and scripts.

## Features

- **TPM, Secure Boot, and RAM Checks Bypassed**: The configuration includes registry tweaks to bypass TPM, Secure Boot, and RAM checks for systems that do not meet the hardware requirements for Windows.
  
- **Custom User and Timezone Setup**: 
  - Default user: `usop` password: `8250` with administrative privileges.<mark>Highlighted text</mark>
  - Timezone: `India Standard Time`.
  
- **Automatic Application and Feature Removal**: 
  - Removal of pre-installed Windows applications such as Bing Search, Camera, OneDrive, Cortana, etc.
  - Removal of Windows features like Internet Explorer, Paint, and Snipping Tool.

- **Auto Logon**: The system is configured to automatically log in with the user `usop` once after installation.

- **Taskbar and Start Menu Customization**: Removes unnecessary taskbar icons and customizes the Start Menu layout.

- **Disable SmartScreen and UAC**: The configuration disables Windows SmartScreen and User Account Control (UAC) for a smoother installation and operation.

- **PowerShell Scripts**: 
  - `remove-packages.ps1`: Removes unwanted provisioned apps.
  - `remove-caps.ps1`: Disables Windows capabilities.
  - `remove-features.ps1`: Disables optional features.
  - `DeleteTaskbarIcons.ps1`: Deletes default taskbar icons.
  - `SetWallpaper.ps1`: Sets a solid color wallpaper (#b50d0d).
  - `MakeEdgeUninstallable.ps1`: Modifies Edge policies to make it uninstallable.

## Usage

1. Clone this repository or copy the `autounattend.xml` to the root of your bootable Windows installation media.
2. Boot from the media, and Windows will automatically apply the settings during installation.
3. After installation, all unnecessary apps, features, and capabilities will be removed based on the included PowerShell scripts.

## License

This project is licensed under the MIT License. See the `LICENSE` file for more details.
