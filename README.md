# Make-Manual

Windows installers and OTA packages for MakeManual. Application source is maintained in the private `kangwang47/www` repository under `MakeManual/`.

Each stable release provides:

- `MakeManual-<version>-Setup.exe` — per-user Windows installer.
- `MakeManual-<version>-Update.zip` — files used by the in-app OTA updater.
- `manifest.json` — versioned download URL, file size, and SHA-256 digest.

The app checks `releases/latest/download/manifest.json`, verifies the package size and SHA-256, then invokes its separately installed updater. User manuals remain under `%LOCALAPPDATA%\MakeManual` across application updates.
