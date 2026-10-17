# Windows compatibility — v3.1.0

## What changed

The previous ZIP restricted its manifest to Illustrator 2026 and used only CEP 12. Version 3.1.0 allows Illustrator 23.x–30.x, requires CEP 9 or later, detects matching runtimes, and installs in the shared per-user CEP folder. Spacing and keyboard-focus styles include fallbacks for older embedded browsers.

| Illustrator | Application version | CEP setting |
| --- | --- | --- |
| 2019 | 23.x | CSXS.9 |
| 2020 | 24.x | CSXS.9 |
| 2021 before 25.3 | 25.0–25.2.x | CSXS.10 |
| 2021 from 25.3 | 25.3+ | CSXS.11 |
| 2022–2024 | 26.x–28.x | CSXS.11 |
| 2025 before 29.5.1 | 29.0–29.5.0 | CSXS.11 |
| 2025 from 29.5.1 | 29.5.1+ | CSXS.12 |
| 2026 | 30.x | CSXS.12 |

These are compatibility targets, not a claim of testing every release. Only Illustrator 2026 / 30.6.0 is available on the development computer. Actual menu loading, docking and operation in 2020 and 2025 still need verification on those applications. CS6, CC 2014–2018, future versions and macOS are outside this Windows package's scope.

The runtime boundaries follow [Adobe's CEP host compatibility table](https://github.com/Adobe-CEP/CEP-Resources/blob/master/CEP_12.x/Documentation/CEP%2012%20HTML%20Extension%20Cookbook.md). Earlier CEP engines use older Chromium versions, so the panel avoids relying on flex gap and focus-visible alone.

## Custom installation path

The installer checks standard Adobe folders and registered installation locations. If your installation is not found, open PowerShell in the extracted package folder and provide the actual executable path:

```powershell
.\Install-Windows.ps1 -IllustratorPath 'D:\Adobe\Adobe Illustrator 2020\Support Files\Contents\Windows\Illustrator.exe'
```

If PowerShell blocks local scripts, use the provided wrapper with the same argument:

```powershell
.\Install-Windows.cmd -IllustratorPath 'D:\Adobe\Adobe Illustrator 2020\Support Files\Contents\Windows\Illustrator.exe'
```

Replace the example with your real path. For repair, use `Repair-Blank-Panel` with the same option.

For a diagnostic check without installation or preference changes:

```powershell
.\Install-Windows.cmd -CheckOnly
```

Advanced users can specify the exact application version from Help → About Illustrator. Use application numbers, not the marketing year:

```powershell
.\Install-Windows.cmd -IllustratorVersion 24.0
```

For multiple explicit versions, invoke the PowerShell script inside PowerShell with an array, for example `-IllustratorVersion '24.0','29.0'`. Explicit versions override the detected runtime list. Do not guess the 2025 patch: 29.5.1 switches from CEP 11 to CEP 12.

## Settings and backups

Typing YES enables `PlayerDebugMode`, string `1`, only for the targeted runtimes under `HKCU\Software\Adobe\CSXS.<version>`. This also allows other unsigned extensions using those runtimes for the current user.

Original values are saved in `%LOCALAPPDATA%\Ashad\Guide Layout\settings-receipt.json`. Upgrades retain the original values and add records only for newly detected runtimes. The old single-runtime installer receipt is migrated when available. Previous extension copies are backed up under `Extension backups` in the same directory.

Keep these receipts if you want to restore settings during uninstall. No Illustrator documents are changed by installation or repair. If you later add a different Illustrator version, rerun the installer or repair to detect its runtime.
