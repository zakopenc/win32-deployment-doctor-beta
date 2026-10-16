# Sample logs (fake data)
These IME logs are **synthetic**, not from a real device. They were built from the unit-test templates in `scripts/tests/fixtures/` with fixed dates: 15 Oct 2026 for the main entries, plus one deliberately old line dated 10 Sep 2025. App names (Contoso, Fabrikam) and app IDs are placeholders.

- `problem/`: logs that should produce verdicts (for example KC-001, detection fails after a successful install).
- `healthy/`: logs for an app that installs and is then detected.

Run offline from the repository root. `-DaysBack 365` (the maximum) keeps the 15 Oct 2026 entries inside the window until 15 Oct 2027; the old line stays outside it, as intended:
```powershell
.\scripts\Invoke-DeviceDiagnostic.ps1 -LogPath .\sample-logs\problem -SkipRegistry -DaysBack 365 -OutputPath .\sample-out
.\scripts\Invoke-DeviceDiagnostic.ps1 -LogPath .\sample-logs\healthy -SkipRegistry -DaysBack 365 -OutputPath .\sample-out
```
Open the HTML file written to `.\sample-out`. Nothing is read from this computer's registry and nothing is sent anywhere.

After 15 Oct 2027, or for logs dated yesterday, regenerate fresh copies with this one line (run it from the repository root):
```powershell
. .\scripts\tests\TestHelpers.ps1; New-ZkTestLogFolder -Destination .\sample-logs\fresh -Map @{ 'AppWorkload.log.template' = 'AppWorkload.log'; 'IntuneManagementExtension.log.template' = 'IntuneManagementExtension.log' }
```
Then run with `-LogPath .\sample-logs\fresh -SkipRegistry`.
