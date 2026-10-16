# Credits

## Third-party code
No third-party source code is copied or ported into this repository. The scripts were written from Microsoft Learn / Microsoft Graph documentation. Two MIT projects were used as format or pattern references, and their license files are included in `third-party/` as a courtesy:

| Project | Author | License | How it was used |
|---|---|---|---|
| [adamgell/cmtraceopen](https://github.com/adamgell/cmtraceopen) | Adam Gell | MIT, (c) 2026 | CMTrace record layout read by the log parser (from its documented parser). Parser itself is new code. License: `third-party/cmtraceopen/LICENSE` |
| [MSEndpointMgr/IntuneWin32App](https://github.com/MSEndpointMgr/IntuneWin32App) | MSEndpointMgr | MIT, (c) 2020 | Reference for Win32 app Graph object shapes and the beta `isof('microsoft.graph.win32LobApp')` filter pattern. No code copied. License: `third-party/IntuneWin32App/LICENSE` |

## Link-only tools (not included, no code used)
| Tool | License | Why link-only |
|---|---|---|
| [petripaavola/Get-IntuneManagementExtensionDiagnostics](https://github.com/petripaavola/Get-IntuneManagementExtensionDiagnostics) | No license file | Unlicensed. Not read, not ported. The IME parser is clean-room. |
| [Microsoft Win32 Content Prep Tool](https://github.com/microsoft/Microsoft-Win32-Content-Prep-Tool) | Microsoft terms | Prerequisite only |

Microsoft, Windows, Intune, Entra and Autopilot are trademarks of Microsoft Corporation. ZakitPro is not affiliated with or endorsed by Microsoft.
