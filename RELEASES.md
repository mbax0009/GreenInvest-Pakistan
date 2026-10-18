# Windows releases and verification

## Current official release

| Item | Value |
| --- | --- |
| Product | GreenInvest Pakistan 4.7.1 |
| Platform | 64-bit Windows 10 and 11 |
| Package | `GreenInvest-Windows-x64.zip` |
| Download size | 157.8 MiB |
| Extracted size | 388.1 MiB |
| SHA-256 | `AAE5D2CD2244AF1A26BA7A8DF8987AD4087D9368AF5010CE4EF199E6537BD24A` |

Version 4.7.1 aligns solar and inverter capacity and makes backup power distinct
from battery energy. The result shows PV inverter output, separate backup
inverter power where applicable, and battery storage with explicit units.
A 17.5 kWh battery describes stored energy and duration, not a 17.5 kW inverter.
Backup power is checked against protected running and startup loads.

The tagged build passed all 503 source regression tests, the Chromium consumer
journey and production container checks. The complete Windows ZIP was extracted
on a clean build runner and passed desktop startup and a real calculation.
The downloaded package was independently checked against the private build's
SHA-256 manifest, and its embedded application/model versions were verified.
It requires no separate Python, Node.js or web-hosting account.

## Install

1. Open the [latest release](https://github.com/mbax0009/GreenInvest-Pakistan/releases/latest).
2. Download `GreenInvest-Windows-x64.zip` and the SHA-256 checksum file.
3. Verify the archive.
4. Use Windows **Extract All** and run `GreenInvest.exe` from the extracted folder.

Do not run the executable directly from inside the ZIP. Keep the `_internal`
folder beside `GreenInvest.exe`; it contains the bundled Python, Qt WebEngine,
frontend, reference data, and calculation runtime.

## Verify with PowerShell or Windows Terminal

```powershell
Get-FileHash .\GreenInvest-Windows-x64.zip -Algorithm SHA256
```

Compare the printed hash with the release checksum file.

## Verify with Command Prompt

```bat
certutil -hashfile GreenInvest-Windows-x64.zip SHA256
```

The current public package is a portable 64-bit Windows preview. It is
self-contained but not code-signed. Download it only from the official release
page, and do not use a package whose checksum differs.

The ZIP includes `RELEASE-MANIFEST.txt` and a `THIRD-PARTY-LICENSES` directory
containing the exact bundled dependency manifest and redistribution notices.

[Download the official release](https://github.com/mbax0009/GreenInvest-Pakistan/releases/latest)
or return to the [product overview](README.md).
