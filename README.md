# Sol Agenda — independent hosting

This is the complete static site. No npm install, server code, ChatGPT account, or build command is required to host these files.

## Host on GitHub Pages

1. Create a GitHub repository, for example `sol-agenda`. A GitHub Pages site should be treated as public: do not upload a personal progress backup to this repository.
2. Upload `index.html`, `sol-sun.jpg`, and `.nojekyll` to the **root** of the repository (not a nested `dist` folder). Commit them on the `main` branch.
3. In the repository, go to **Settings → Pages**. Under **Build and deployment**, choose **Deploy from a branch**, then select `main` and `/(root)`, and click **Save**.
4. Open the Pages URL displayed there. For a repository called `sol-agenda`, it normally looks like `https://YOUR-USERNAME.github.io/sol-agenda/`.

To host on another static host, upload the same three files together at the site root. The site uses relative paths, so it also works under a subfolder.

## Transfer your current progress

Your edits, checklists, Forma counts, portraits you uploaded, shards, and polarities are stored in your browser for each web address. Moving the site files does not move that data.

1. In the current Sol Agenda site, open the Overview page and click **Download backup**. Keep the downloaded JSON file private.
2. Open the new hosted address using the same browser and click **Restore backup**, choose that JSON, and confirm. The page will reload with your data.
3. Make another backup whenever you want a copy of subsequent changes. Different devices/browsers need their own restore; the site has no sync server.

The restore replaces matching Sol Agenda saved fields in that browser. It does not erase unrelated browser data.

## Local preview and future changes

From the folder containing `index.html`, run `python3 -m http.server 8000` and open `http://localhost:8000/`. The source is a single HTML file with inline CSS and JavaScript, plus `sol-sun.jpg`. Edit `index.html` and re-upload the changed files to publish an update.

Official Warframe portraits and Google Fonts are requested from their respective external sites when online; personal uploaded portraits remain in browser storage and are carried by the backup JSON. The site itself does not require ChatGPT Sites to run.
