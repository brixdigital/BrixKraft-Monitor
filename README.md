# BrixKraft Monitor

See your internet speed, CPU, RAM, GPU and ping right on the Windows taskbar, and know when your connection drops.

Free for personal use. Made by Joseph Abrique, BrixKraft.

## What it does

On your taskbar, next to the clock:
- Upload and download speed
- CPU, RAM, GPU and disk use (disk is off by default)
- Ping, with a clear warning when you go offline
- Values change color when usage gets high

Click the readout to open the panel:
- 60-second network graph
- Data used today and this month
- Status lights for websites or servers you choose
- Top apps by CPU and RAM, with their open connections

Alerts:
- Daily and monthly data limits, with a warning at 80 and 100 percent
- Internet drops and returns, with an outage history
- A website or server you watch goes down or comes back

Also included: a floating window mode, four color themes, and an optional start with Windows.

## Requirements

- Windows 10 (version 2004 or newer) or Windows 11, 64-bit
- No admin rights, no drivers and no separate .NET install needed

Tested on Windows 11 with one monitor and a dark taskbar. Other setups have not been tested yet.

## Download

1. Go to the [Releases page](../../releases/latest).
2. Under **Assets**, click **BrixKraftMonitor.exe** to download it (about 190 MB).

## Install

There is no installer. The app is a single file.

1. Make a folder for it, for example `C:\Users\<your name>\Apps\BrixKraft Monitor`.
2. Move **BrixKraftMonitor.exe** from your Downloads folder into it. Keep it there: if you turn on Start with Windows, Windows starts it from this spot.
3. Double-click **BrixKraftMonitor.exe**.
4. Windows may show **"Windows protected your PC"**. This appears because the app is not digitally signed yet. Click **More info**, then **Run anyway**. You only need to do this once.
5. The readout appears on the taskbar, to the left of the system tray icons. A BrixKraft icon also appears in the system tray.

If you prefer to check the file first, compare its SHA-256 hash with the one on the Releases page. In PowerShell:

```
Get-FileHash .\BrixKraftMonitor.exe
```

## How to use it

**Taskbar readout**
- **Left-click** it to open or close the panel.
- **Right-click** it for the menu: Open panel, Settings, Exit.
- The same menu is on the BrixKraft icon in the system tray.

**Settings** (right-click, then Settings). Click **Save** after changing anything.

| Tab | What you can set |
|---|---|
| Display | Which values show on the readout, floating window mode, gap from the system tray, text size, theme, Start with Windows |
| Internet and alerts | The address to ping (default 1.1.1.1), outage alerts, daily and monthly data limits, the day your month resets |
| Status lights | Add web addresses to watch, for example your website or `http://localhost:5678`. Each is checked every 60 seconds |
| History | Data used over the last 30 days and past internet outages |
| About | Version and author |

**Tips**
- If the readout covers your taskbar icons, raise **Gap from the system tray** in Display, or switch to the floating window.
- In floating mode, drag the window to move it and double-click it to open the panel.
- To start the app when you sign in, tick **Start with Windows** in Display and click Save.

## Update

1. Right-click the readout and click **Exit**.
2. Download the new **BrixKraftMonitor.exe** from Releases and replace the old file in the same folder.
3. Start it again. Your settings and history are kept.

## Uninstall

1. If you turned on Start with Windows, untick it in Settings and click Save.
2. Right-click the readout and click **Exit**.
3. Delete **BrixKraftMonitor.exe**.
4. To remove your settings and history too, delete the folder `%LOCALAPPDATA%\BrixKraft\Monitor` (paste that into the File Explorer address bar).

## Privacy

Your settings, data usage and outage history are saved only on your PC. There is no account, no analytics and no BrixKraft server. The app only connects to:
- the address you set for the internet check (a ping every 5 seconds, default 1.1.1.1), which you can change or turn off
- the status light addresses you add yourself

Full policy: [PRIVACY.md](PRIVACY.md)

## Known limits

- The readout shows on the main monitor's taskbar only.
- It does not reserve taskbar space, so it can overlap icons when many are open. Use the gap setting or floating mode.
- A Windows update could change the taskbar and break the placement. Floating mode still works.
- Temperatures are not included, because they need a system driver.
- Per-app bandwidth is not included.

## Problems and suggestions

Open an issue on the [Issues page](../../issues), or email brixkraft@gmail.com.

## License

Free to use. See [LICENSE.txt](LICENSE.txt). The source code is not public.

Copyright (c) 2026 Joseph Abrique, BrixKraft.
