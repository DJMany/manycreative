# ManyCreative — Static Site (Ready to Upload)

This version needs **no terminal and no scripts**. Images load directly from
your existing Squarespace CDN links, so the site works the moment you upload
it to GitHub.

## Get it live (all in the browser)

1. Go to https://github.com/new
   - Repo name: `manycreative` (or `YOURUSERNAME.github.io` for a shorter URL)
   - Visibility: **Public**
   - Click **Create repository**
2. On the new repo page, click **uploading an existing file**
   (or **Add file → Upload files**).
3. Drag in everything from this folder: `index.html`, `home.html`,
   `places.html`, `people.html`, `about.html`, the `css` folder,
   `download-images.sh`, and this README. Click **Commit changes**.
4. Go to **Settings → Pages**. Under "Build and deployment":
   - Source: `Deploy from a branch`
   - Branch: `main`, folder `/ (root)` → **Save**
5. Wait 1–2 minutes, refresh the Pages settings page, and your live link
   appears at the top: `https://YOURUSERNAME.github.io/manycreative/`

## Important: before you ever cancel Squarespace

The images currently load from Squarespace's servers. If you cancel your
Squarespace subscription, those links stop working and the photos disappear.

Before cancelling, run the included `download-images.sh` on your computer
(from a terminal: `bash download-images.sh` inside this folder). It saves
every photo into an `images/` folder. Then:

1. Upload the `images` folder to the GitHub repo the same drag-and-drop way.
2. Ask Claude (or edit yourself) to switch the pages back to the local
   `images/...` paths.

Until then, the hotlinked version works fine — no rush.

## Optional: use your manycreative.com domain

1. Repo **Settings → Pages → Custom domain** → enter `manycreative.com` → Save
2. At your domain registrar (wherever manycreative.com is registered), add:
   - Four `A` records for the root domain: `185.199.108.153`,
     `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - A `CNAME` record: host `www` → `YOURUSERNAME.github.io`
3. Back in Settings → Pages, tick **Enforce HTTPS** once available.
