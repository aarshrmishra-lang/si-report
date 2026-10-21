SI Vessel Attendance Report app (OMP-17-01H) — v1.0.0
=========================================================

WHAT IT IS
An installable web app (PWA). One code base runs on Android, iPhone/iPad, Windows, Mac and ChromeOS.
It works fully offline after the first open. Reports and photos stay on the device (browser storage).

DEPLOY (needs any HTTPS static host; installing requires HTTPS)
  Option A  Netlify Drop: drag this whole folder onto https://app.netlify.com/drop
  Option B  GitHub Pages: push the folder to a repo, Settings > Pages > deploy from branch.
  Option C  Company intranet / IIS / SharePoint static site served over HTTPS.
  No server code, database or build step is needed. Upload the files as they are.

INSTALL ON DEVICES
  Android (Chrome):    open the link > menu > "Install app" (or the Install button in the app bar).
  iPhone/iPad (Safari): open the link > Share > "Add to Home Screen".
  Windows/Mac (Chrome or Edge): open the link > install icon in the address bar.

SYNC BETWEEN DEVICES
  Wi-Fi (direct, no internet): both devices on the same Wi-Fi or a phone hotspot.
    Device 1: Sync > Wi-Fi > Start (shows a QR code). Device 2: Sync > Wi-Fi > Join, scan it,
    then let device 1 scan the reply QR. All reports and photos merge both ways.
    If a camera is not available, copy/paste the code text instead.
  Bluetooth / file: Sync > Bluetooth / file > "Send via Bluetooth / share" (phone share sheet:
    Bluetooth, Quick Share/Nearby Share, AirDrop) or "Save sync file". On the other device: Import sync file.
  Merging is field by field; the most recent edit of each field or photo wins.

UPDATING THE APP
  Replace the files on the host and change CACHE version in sw.js. Devices pick up the new version
  next time they open the app online. Reports already on devices are kept.

FILES
  index.html            the app (includes the original OMP-17-01H Word form as its template)
  sw.js                 offline cache
  manifest.webmanifest  install settings
  icons/                app icons
