EXPENSE SHEET - installable web app

WHAT IS IN THIS FOLDER
  index.html            the whole app
  sw.js                 makes it work offline
  manifest.webmanifest  + icon-*.png, apple-touch-icon.png   home-screen install
  fonts/                the app's fonts (kept so it works offline)
Everything uses relative paths, so it works from any folder or sub-path of a static host.

FIRST-TIME SETUP ON GITHUB (do this once)
  1. On your repository page choose  Add file > Upload files.
  2. On your computer, open this unzipped folder, select EVERYTHING inside it (including the fonts folder)
     and drag it into the upload box. Wait until all files are listed.
  3. Under "Commit changes" leave "Commit directly to the main branch" ticked and press Commit changes.
  4. Repository Settings > Pages > Source: "Deploy from a branch" > Branch: main, folder: / (root) > Save.
     (On the free GitHub plan the repository must be Public for Pages to work.)
  5. After about a minute the Pages screen shows "Your site is live at https://<you>.github.io/<repo>/".

INSTALL ON YOUR PHONE
  Android (Chrome):  open the address > menu (three dots) > Install app / Add to Home screen.
  iPhone (Safari):   open the address > Share > Add to Home Screen.
  On iPhone install FIRST, then enter or import data inside the installed app - Safari and the
  home-screen app keep separate storage.

UPDATING THE APP (every time you get a new version)
  1. Download the new zip and unzip it.
  2. Repository page > Add file > Upload files > drag in the files (all of them is fine; GitHub only
     records what actually changed. Usually only index.html changes and you can upload just that one file -
     a file with the same name replaces the old one).
  3. Press Commit changes (message such as "Update app").
  4. Wait about a minute. In the repository open the Actions tab: when the latest "pages build and
     deployment" run shows a green tick, the new version is live.
  5. Open the app (close it fully and reopen if it is already running). Check Settings > version line at the
     bottom to confirm you are on the new version.
  Your entries are stored on the device and are not touched by updates.

IMPORTANT
  - Do not rename the repository or your GitHub username: the app's address would change and an app at a new
    address starts empty (use Settings > Export CSV, then Import CSV at the new address, if that ever happens).
  - Export a CSV now and then as a backup (Settings > Export CSV).
  - Only if you change icons or fonts: also change CACHE_VERSION at the top of sw.js (v1 -> v2).
