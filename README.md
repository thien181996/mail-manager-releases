# Mail Manager — Smart Email Workspace

Windows desktop email client for Gmail and Microsoft (Outlook.com, Hotmail, Live, Microsoft 365) accounts.
This repository hosts the signed download packages. Every release is published under its own version tag.

**Latest download:** see the [Releases](../../releases) page.

---

## Installer

| | |
|---|---|
| Package type | `.exe` (NSIS) |
| Architecture | x64 |
| Scope | Per-user (no administrator rights required) |
| Default install folder | `%LOCALAPPDATA%\Programs\mail-manager` |
| User data | `%APPDATA%\Mail Manager` (kept when upgrading, removed on request at uninstall) |

### Silent installation

```
MailManager-Setup-<version>.exe /S
```

To install into a specific folder, add `/D` as the **last** switch, unquoted even if the path contains spaces:

```
MailManager-Setup-<version>.exe /S /D=C:\Program Files\Mail Manager
```

Silent uninstall:

```
"%LOCALAPPDATA%\Programs\mail-manager\Uninstall Mail Manager.exe" /S
```

### Installer return codes

The installer uses the standard NSIS exit codes. No custom codes are defined.

| Code | Meaning | What to do |
|---|---|---|
| `0` | Installation completed successfully. | Nothing. Mail Manager is installed. |
| `1` | Installation was cancelled by the user, or the installer could not start (for example, another instance of the installer is already running, or a required file was blocked). | Run the installer again. If it was blocked, check SmartScreen / antivirus and that the downloaded file is complete. |
| `2` | Installation failed. The installer aborted while copying or registering files. | Make sure Mail Manager is not running, there is free disk space on the target drive, and the install folder is writable. Then run the installer again. |

The uninstaller uses the same codes.

### Upgrading

Running a newer installer over an existing installation removes the previous version first and keeps all user data: mail stored on the device, settings, signatures, rules, workflows and the signed-in accounts. No separate uninstall step is needed.

---

## System requirements

- Windows 10 version 1809 (64-bit) or later, or Windows 11
- 4 GB RAM minimum, 8 GB recommended
- About 400 MB of free disk space, plus space for cached mail and attachments
- Internet connection; a keyboard and a mouse

## Languages

English, Vietnamese, Chinese (Simplified), Japanese.

## Privacy

All data is stored locally on the device and encrypted with AES-256; the key is protected by Windows Data Protection (DPAPI). The app connects only to Google (Gmail API) and Microsoft (Microsoft Graph). No analytics, telemetry or advertising. See the [Privacy Policy](../docs/privacy-policy.md).

## Support

Phan Ngọc Thiện — thien181996@gmail.com
