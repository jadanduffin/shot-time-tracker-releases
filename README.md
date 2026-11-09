# Shot Tracker releases

Installers for Shot Tracker. Download ShotTracker-Setup.exe from the latest release.

## Known issues

### The window goes black a few seconds after opening

**Cause:** RivaTuner Statistics Server (installed with MSI Afterburner) hooks its on-screen overlay into the web
engine Shot Tracker draws with (`msedgewebview2.exe`), and on some launches that crashes it. Your timers keep
running and nothing is lost: closing the black window stops them and saves.

**Fix:** tell RivaTuner to leave the web engine alone.

1. Open RivaTuner Statistics Server from the system tray.
2. Click **Add** (bottom left) and pick `msedgewebview2.exe`. It is usually in
   `C:\Program Files (x86)\Microsoft\EdgeWebView\Application\<version>\`.
3. With that profile selected, set **Application detection level** to **None**.
4. Restart Shot Tracker.

If the window is already black, close Shot Tracker and open it again.
