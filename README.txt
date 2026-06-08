IRONLOG — standalone offline gym logger
=======================================

This folder is a complete Progressive Web App (PWA). Once it's on a web
address and you "Add to Home Screen", it runs fully offline like a native app.
All your data is stored on your phone (localStorage) — nothing leaves the device.

FILES
  index.html            the whole app
  manifest.webmanifest  app name + icons (makes it installable)
  sw.js                 service worker (caches everything for offline use)
  icon-192.png          app icons
  icon-512.png

WHY IT NEEDS A URL
  Service workers (the offline magic) only work over https:// — not from a
  file on disk. So you upload these 5 files to any free static host, open the
  link once on your phone, then add it to your home screen. After that first
  visit, no internet is ever needed.

EASIEST DEPLOY (GitHub Pages, free, permanent)
  1. Make a free github.com account.
  2. Create a new repository, e.g. "ironlog". Make it Public.
  3. Click "Add file" > "Upload files" and drag in all 5 files. Commit.
  4. Repo Settings > Pages > "Deploy from a branch" > main / root > Save.
  5. Wait ~1 min. Your app is live at:
       https://YOURNAME.github.io/ironlog/

INSTALL ON PHONE
  iPhone (Safari):  open the link > Share button > "Add to Home Screen".
  Android (Chrome): open the link > menu (⋮) > "Install app" / "Add to Home screen".

  Launch it from the home screen icon. Turn off wifi/data to confirm it works
  offline — it will.

BACKUP
  Tap the gear (top-right) > "Export backup" now and then to save a JSON file.
  If you switch phones or clear your browser, "Import backup" restores everything.
