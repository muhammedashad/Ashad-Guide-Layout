# Ashad Guide Layout

**Free margins, columns and rows for Adobe Illustrator on Windows.**

Create layouts with live preview in a dockable Illustrator panel.

**Version 3.1.0 · Windows · Compatibility target: Illustrator 2019–2026**

## Download

**[Download Ashad Guide Layout for Windows — v3.1.0](https://github.com/muhammedashad/Ashad-Guide-Layout/raw/refs/heads/main/Ashad-Guide-Layout-Windows-v3.1.0.zip)**

This update removes the 2026-only restriction. It includes Illustrator **2020 (24.x)** and **2025 (29.x)** in its allowed range and detects the correct CEP setting for each installed version. Older Illustrator versions have not been tested in the actual applications; see [compatibility and testing](COMPATIBILITY.md).

![Ashad Guide Layout panel in Illustrator 2026](extension-preview.png)

## Before you start

Save your work and close **all Illustrator versions**. Download the ZIP, right-click it → **Extract All** → **Extract**, then open the extracted folder. Keep all package files together.

## 1. Run Install-Windows first

![Install-Windows file](install-windows-file.png)

1. Double-click **Install-Windows.cmd**. Windows may show only **Install-Windows**.
2. The installer lists the Illustrator versions it finds.
3. Read the prompt, type **YES**, then press **Enter**.
4. Wait for **Installed**.
5. Restart Illustrator. Choose **Window → Extensions → Ashad Guide Layout**.

The installer puts the panel in a shared folder for your Windows account:

```text
%APPDATA%\Adobe\CEP\extensions\com.ashad.guidelayout
```

This location works across the targeted Illustrator versions. It normally needs no administrator access. The installer also enables unsigned panels for the detected CEP versions; this allows other unsigned panels using those runtimes for your Windows account. Previous settings and the previous per-user panel are backed up.

**If the panel opens, you are finished. Skip sections 2 and 3.**

Installing another Illustrator version later? Run this installer again so it can detect that version too.

## 2. Manual folder copy — optional alternative

Use this only instead of the installer. Do not keep duplicate installations in different folders.

![The complete extension folder to copy](extension-folder.png)

1. Copy the entire **com.ashad.guidelayout** folder from the new ZIP.
2. Press **Windows + R**, paste `%APPDATA%\Adobe\CEP\extensions`, and press **Enter**. If the folder does not exist, open `%APPDATA%\Adobe` and create `CEP`, then `extensions` inside it.
3. Paste **com.ashad.guidelayout** inside **extensions**. Back up an existing copy outside the extensions folder before replacing it.
4. Run the repair in section 3 to enable the matching unsigned-panel settings.

Check the folder structure:

```text
extensions
└── com.ashad.guidelayout
    ├── CSXS
    │   └── manifest.xml
    ├── index.html
    └── other extension files
```

**Upgrading from the old 2026-only instructions:** a copy in `C:\Program Files\Adobe\Adobe Illustrator 2026\Support Files\Required\CEP\extensions` is specific to that application. Close Illustrator and move only your old **com.ashad.guidelayout** folder to a backup location outside any CEP extensions folder, then use the installer above. Do not move or remove other extensions. Windows may require administrator permission for the old Program Files copy.

## 3. Run Repair-Blank-Panel last — only if needed

Use repair after manual installation, or when the installed extension is missing or blank.

![Repair-Blank-Panel file](repair-blank-panel-file.png)

1. Save your work and close all Illustrator versions.
2. In the extracted **v3.1.0** package, double-click **Repair-Blank-Panel.cmd**.
3. Read the detected CEP versions and unsigned-panel notice. Type **YES** and press **Enter**.
4. Wait for **REPAIR SETTING VERIFIED**.
5. Restart Illustrator and open **Window → Extensions → Ashad Guide Layout**.

Keep **Compatibility.ps1** and the matching `.ps1` scripts beside the `.cmd` files. Repair checks the installed files and enables the matching settings. It cannot turn an old 3.0.2 panel into a compatible one: install the complete new ZIP first.

## Create a layout

1. Open an Illustrator document.
2. Choose a preset, artboards and units.
3. Set the margins; use **Link all sides** for equal margins.
4. Enable columns or rows and set count and gutter. Leave width or height blank for automatic sizing.
5. Check **Preview**, then click **Create guides**.

Turn Preview off before saving or closing the document. Native guides follow Illustrator's guide-colour preference. Use **Editable lines** for coloured lines that appear in exports.

## Troubleshooting

| Problem | Fix |
| --- | --- |
| Shows only in Illustrator 2026 | Install **v3.1.0**, use the shared user folder above, and restart every Illustrator version. Back up old application-folder copies outside CEP folders. |
| Installer cannot find Illustrator | See the [custom installation path instructions](COMPATIBILITY.md#custom-installation-path). |
| Panel missing or blank after installation | Close Illustrator, run the new repair script, then restart. If it persists, send Ashad the exact Illustrator version and error. |
| Missing package files | Extract the complete ZIP. Do not run scripts inside the ZIP or copy only one script. |
| Guides invisible | Choose **View → Guides → Show Guides** and check layer visibility. |
| Layout does not fit | Reduce margins, gutters or the number of columns/rows. |

An organisation may block scripts or unsigned extensions. Contact its administrator if installation is blocked. Repair cannot fix every cause of a blank panel.

## Update or uninstall

**Update:** close Illustrator and run the new **Install-Windows.cmd**. It backs up the previous per-user panel.

**Uninstall:** close Illustrator, run **Uninstall-Windows.cmd**, and type **YES**. Press **Enter** to keep CEP settings for other extensions, or type **RESTORE** to restore saved values. Restoring them may affect other unsigned panels. The uninstaller removes only its per-user installation; manual application-folder copies remain.

## Share and contact

Share this page or the complete **Ashad-Guide-Layout-Windows-v3.1.0.zip** with your friends.

[WhatsApp](https://wa.me/918590956012) · [Instagram](https://www.instagram.com/as.hxd/) · [Behance](https://www.behance.net/muhammedashad) · [LinkedIn](https://www.linkedin.com/in/muhammed-ashad-79a329388) · [Pinterest](https://in.pinterest.com/muhammedashad2005/)

+91 8590956012 · muhammedashad2005@gmail.com

[Compatibility](COMPATIBILITY.md) · [Test report](TEST-REPORT.md) · [Download checksum](https://github.com/muhammedashad/Ashad-Guide-Layout/blob/main/SHA256SUMS.txt) · [Use and sharing permission](COPYRIGHT.txt)

© 2026 Ashad. Complete, unmodified copies may be installed, used and shared with the included notice. This is an independent extension; Adobe and Illustrator belong to their respective owners.

