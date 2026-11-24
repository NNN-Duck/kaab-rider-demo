KAAB RIDER PRO v4.6 - Angry Duck / Stats Backup Edition

Deploy all files together to the same HTTPS static host and path. Back up JSON first, especially before updating or changing origin. To test locally: python -m http.server 8000, then open http://localhost:8000. Use Safari > Share > Add to Home Screen or Android Chrome > Install app. Offline support depends on external libraries being cached after an online visit.

DEVICE MIGRATION
1. On the old device, open Stats (bottom navigation), scroll to Backup & Restore and download or share the JSON backup. This exports all dates, trips, expenses, oilKm, daily goal, last app/payment method and sunlight mode.
2. Transfer the JSON file privately to the new device (Files, AirDrop, Drive, iCloud, etc.).
3. Open the web app on the new device, go to Stats > Backup & Restore, choose the JSON file, check the preview, confirm the checkbox and import. Existing records will be replaced, not merged. Back up any existing data first.
4. Verify History and Stats after import. Keep the original backup file until verified.
Legacy v4.0-v4.3 backups are supported; settings absent in old backups remain unchanged. CSV is for reports, not restoring. There is no server or automatic cross-device sync. Backup JSON is not encrypted. Avoid public sharing.

HOME SCREEN ICON FIX (v4.6)
Upload EVERY file in this ZIP into the same directory as the existing index.html on your HTTPS web host. Do not change the domain or path unnecessarily. The actual home-screen icon is a served PNG, not the embedded header image. A new filename avoids many stale icon cache issues. The conventional apple-touch-icon.png is also included; if the app is hosted in a subdirectory, the explicit relative link still works. If you control the domain root you may also place a copy of apple-touch-icon.png there, provided it will not override a different app's icon.
1. Back up JSON from Stats first. On a previously installed iOS web app, export from that app before removing its icon; storage may be separate from Safari.
2. Open https://YOUR-HOST/YOUR-PATH/apple-touch-icon-v46.png in Safari. It must display the duck PNG, not an HTML page, 404, or login. Verify manifest-v46.webmanifest is served as JSON and Android icons are accessible too.
3. Open the real website URL (not an editor preview, file://, blob:, iframe or share-file link) in Safari. Reload. Share > Add to Home Screen. If offered, keep Open as Web App enabled. Check the preview shows the duck before tapping Add.
4. If an old shortcut keeps the K icon, create a new shortcut after updating. Only remove the old installation after backing up and verifying the new one and restoring data if needed. Do not clear Safari website data or uninstall before backup.
5. If your platform accepts only pasted HTML and cannot host PNG/manifest files, you must use a static HTTPS host or supported public file URLs. An embedded Base64 header image does not reliably supply the iOS home screen icon across versions. The supplied project is not deployed to your host automatically.
Android: Chrome > Install app / Add to Home Screen. The manifest points to versioned PNG icons.
