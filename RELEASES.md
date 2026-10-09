# Windows releases and verification

## Current official release

| Item | Value |
| --- | --- |
| Product | GreenInvest Pakistan 4.6.0 |
| Platform | 64-bit Windows 10 and 11 |
| Package | `GreenInvest-Windows-x64.zip` |
| Download size | 157.3 MiB |
| Extracted size | 386.7 MiB |
| SHA-256 | `52B17CF426F8F0D9991E9CBF8A265B8A95F05759967DF84F6A224DF5516CC80C` |

Version 4.6.0 includes offline equipment prices observed on 9 October 2026,
five price bands, individual component choices and recurring bill-charge inputs.
The complete ZIP was extracted and tested for desktop startup and a real
market-average recommendation before publication. It requires no separate
Python, Node.js or web-hosting account.

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
