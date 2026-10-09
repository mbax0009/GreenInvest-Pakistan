# Windows releases and verification

## Current official release

| Item | Value |
| --- | --- |
| Product | GreenInvest Pakistan 4.7.0 |
| Platform | 64-bit Windows 10 and 11 |
| Package | `GreenInvest-Windows-x64.zip` |
| Download size | 157.4 MiB |
| Extracted size | 386.8 MiB |
| SHA-256 | `9DD93E9B44D3343B9A3D340360CE165B19E45AF065FA88F9460DC41F48C7488B` |

Version 4.7.0 brings the complete decision-studio redesign to Windows: six
guided calculator chapters, an editable review and seven redesigned report
sections, with one navigation menu at a time. Pricing choices, saved plans,
downloads, detailed battery analysis and click-to-run sensitivity and Monte
Carlo are retained. The calculation engine and tariff/pricing reference data
are unchanged from 4.6.0.

The complete ZIP was extracted and tested on a clean Windows build runner for
desktop startup and a real recommendation before publication. The downloaded
archive was independently checked against the build's SHA-256 checksum. It
requires no separate Python, Node.js or web-hosting account.

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
