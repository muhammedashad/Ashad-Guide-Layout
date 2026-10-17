# Manual installation — Windows

[← Back to the main guide](README.md)

Use this method only if you want to copy the folder yourself. If you used **Install-Windows.cmd**, you can skip this guide. **com.ashad.guidelayout is a folder**, not a single file. These pictures illustrate the steps; the extension screenshot at the end shows the real panel.

### 1. Download, close Illustrator and extract

Download **Ashad-Guide-Layout-Windows-v3.0.2.zip**. Save your documents and close Illustrator. Right-click the ZIP → **Extract All** → **Extract**, then open the extracted folder.

![Step 1: download the Windows ZIP, close Illustrator and extract all files](manual-01-extract.svg)

### 2. Copy com.ashad.guidelayout

Inside the extracted package, select the complete **com.ashad.guidelayout** folder. Right-click → **Copy**, or press **Ctrl + C**. Keep all its contents together.

![Step 2: copy the complete com.ashad.guidelayout folder](manual-02-copy.svg)

### 3. Paste into the Illustrator CEP extensions folder

In File Explorer, paste this full path into the address bar and press **Enter**:

```text
C:\Program Files\Adobe\Adobe Illustrator 2026\Support Files\Required\CEP\extensions
```

Press **Ctrl + V** to paste **com.ashad.guidelayout** here. Windows may ask for administrator permission; choose **Continue** if you have permission to install on this computer. If an older copy already exists, back it up outside the extensions folder before replacing it. If Illustrator is installed elsewhere, use its corresponding **Support Files\Required\CEP\extensions** folder.

![Step 3: paste the folder into the Illustrator 2026 CEP extensions directory](manual-03-paste.svg)

### 4. Check the folder structure

The final manifest location must be:

```text
C:\Program Files\Adobe\Adobe Illustrator 2026\Support Files\Required\CEP\extensions\com.ashad.guidelayout\CSXS\manifest.xml
```

The **index.html** file must be directly inside **com.ashad.guidelayout**. Do not paste the entire ZIP package folder here, or nest a second **com.ashad.guidelayout** folder inside the first.

![Step 4: verify the manifest and index.html locations](manual-04-check.svg)

### 5. Enable the unsigned panel

Return to the extracted package and double-click **Repair-Blank-Panel.cmd**. Keep **Repair-Blank-Panel.ps1** beside it. Wait for **REPAIR SETTING VERIFIED**. This repair checks the installed files and enables unsigned CEP 12 panels for your Windows account; it does not copy or reinstall the extension. This setting permits all unsigned CEP 12 panels for your Windows account, not only Ashad Guide Layout.

![Step 5: run Repair-Blank-Panel.cmd and wait for REPAIR SETTING VERIFIED](manual-05-enable.svg)

### 6. Restart Illustrator and open the panel

Start Illustrator, then choose **Window → Extensions → Ashad Guide Layout**. Drag its tab beside your other panels to dock it. Open a document to use the layout controls.

![Step 6: open Window, Extensions, Ashad Guide Layout](manual-06-open.svg)

**What the extension looks like in Illustrator:**

![Ashad Guide Layout panel running in Illustrator](extension-preview.png)

If you already installed a per-user copy with **Install-Windows.cmd**, updating that copy with the installer is simpler than keeping two installations. A higher-version per-user copy can take precedence over the application-folder copy. Illustrator updates or reinstalls may remove files placed inside its application folder. To uninstall a manual copy, close Illustrator and remove only its **com.ashad.guidelayout** folder; the packaged uninstaller handles only installations made by the installer.
