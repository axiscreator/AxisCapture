# AxisCapture

**Capture your AUT scan screens in one keypress, already named and saved as images.**

AxisCapture is a small Windows tool that sits on top of your AUT Solutions window. Press **F8** and it saves two pictures for you: the full workspace and the C-scan. The names count up automatically (S1, S2, S3...) so they are ready to import into AxisBuilder.

## Download

### [Download AxisCapture.exe](../../releases/latest/download/AxisCapture.exe)

Prefer to see the version number and what's new first? Open the [latest release page](../../releases/latest).

- Works on Windows 10 and 11
- Nothing to install. Save the file anywhere and double-click it.

## If Windows shows a blue warning

The first time you run it, Windows may say **"Windows protected your PC."** This is normal for small tools that are not code-signed. To continue:

1. Click **More info**
2. Click **Run anyway**

You only need to do this once.

## How to use it

**One-time setup (about 2 minutes)**

1. Open your AUT Solutions scan screen and start AxisCapture.
2. Click **Setup**, then **Run Guided Setup**.
3. Follow the prompts: choose your image folder, click inside the AUT window, then draw the full-workspace area, the C-scan area, and the safe blank point.

AxisCapture remembers these settings, so you won't repeat this.

**Every scan after that**

1. Click inside the AUT window.
2. Press **F8**.
3. Done. Two images are saved in your folder and the next names are ready.

## Handy features

| Feature | What it does |
|---|---|
| **Quick mode** | Tick the box and F8 saves right away with the next number. Hold **Shift + F8** if you want to type your own names. |
| **Delete last** | Mistake? Sends the last two images to the Recycle Bin and reuses their names. |
| **Open folder** | Jumps to your images folder. |
| **JPG or PNG** | Saves smaller JPG files by default. Switch to PNG in Setup > Options if you need lossless. |
| **Change the hotkey** | Don't like F8? Pick another in Setup > Options. |
| **Session log** | A list of every capture (time, file names, window) is saved in your folder as `AxisCapture_Log.csv`. |

## Good to know

- Your settings are stored on your own PC, in `%APPDATA%\AUTCaptureAssistant`. Nothing about you or your scans is sent anywhere.
- **Updates:** at startup AxisCapture asks GitHub whether a newer version exists. If one does, it offers to open the download page. Download the new `AxisCapture.exe`, close the old one, and replace the file. Your settings carry over. Turn the check off in Setup > Options, or check by hand with right-click on the top strip > Check for updates now.
- If you save over a name that already exists, the old files go to the Recycle Bin, so you can get them back.
- Using AxisBuilder? Point it at the same folder and it will pick up the images.

## Check your download (optional)

To confirm the file wasn't changed, open PowerShell in the folder with the download and run:

```
Get-FileHash .\AxisCapture.exe
```

The result should match the checksum shown on the release page for your version.

## Updating

Download the newest version from the link above and replace your old `AxisCapture.exe`. Your settings carry over automatically.
