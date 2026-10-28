# MementoSift releases

Release packages of **MementoSift**, a local-first photo archive organizer for Windows: duplicates and near-duplicates, capture dates, year/day folders, people (faces), tags and names written back into the files. Nothing leaves your computer.

This repository holds only the packages; the source code lives in the private `MementoSift` repository. The app's update check reads the newest release here once a day (version number only).

## Install

Every release has three files:

| file | what |
|---|---|
| `MementoSift-Setup-x.y.z.exe` | Windows 10/11 x64 installer. Installs the WebView2 runtime when missing; can install ffmpeg and exiftool through winget (optional). |
| `MementoSift-x.y.z-portable.zip` | No installation: unpack and start `MementoSift.exe`. Needs the WebView2 runtime (Windows 11 and Edge already have it). |
| `SHA256SUMS-x.y.z.txt` | Checksums of both packages. |

Verify a download in PowerShell:

```powershell
Get-FileHash .\MementoSift-Setup-x.y.z.exe -Algorithm SHA256
```

exiftool is needed to write dates, tags and names into files; ffmpeg for video previews and conversion. Without them those features stay off; everything else works.

## Licence

MIT. Third-party components and their licences are listed in the app (About page) and in `THIRD-PARTY-NOTICES.txt` next to the program.
