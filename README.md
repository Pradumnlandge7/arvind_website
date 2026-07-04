# KhetKart — Setup Guide (simple steps)

You got 4 files:
- `index.html` → the public website (farmers see this)
- `admin.html` → your brother's admin page (only he uses this)
- `products.json` → starts empty, admin panel fills it automatically
- `ads.json` → starts empty, admin panel fills it automatically

You don't need to touch `products.json` or `ads.json` by hand — the admin page updates them for you.

---

## Step 1: Put the files on GitHub

1. Go to [github.com](https://github.com) and make a free account (if you don't have one).
2. Click **New repository**. Name it anything, e.g. `khetkart`. Keep it **Public**. Click **Create repository**.
3. On the repo page, click **Add file → Upload files**, and upload all 4 files (`index.html`, `admin.html`, `products.json`, `ads.json`).
4. Click **Commit changes**.

## Step 2: Turn on the free website (GitHub Pages)

1. In your repo, go to **Settings → Pages** (left sidebar).
2. Under "Branch", choose `main` and folder `/ (root)`. Click **Save**.
3. Wait about a minute. GitHub will show you a link like:
   `https://yourusername.github.io/khetkart/`
   That's your live website! Bookmark it.
4. Your admin page will be at:
   `https://yourusername.github.io/khetkart/admin.html`
   (Don't share this link with farmers — only your brother should use it.)

## Step 3: Get a GitHub Access Token (so the admin page can save products)

This token lets the admin page save new products directly to your GitHub repo. It only takes 2 minutes:

1. Go to **github.com/settings/tokens?type=beta**
2. Click **Generate new token**.
3. Give it a name like "KhetKart Admin".
4. Under **Repository access**, choose **Only select repositories** → pick your `khetkart` repo.
5. Under **Permissions → Repository permissions**, find **Contents** and set it to **Read and write**.
6. Click **Generate token** and **copy it** (you won't see it again — if you lose it, just make a new one).

## Step 4: Connect the admin page

1. Open your admin link: `https://yourusername.github.io/khetkart/admin.html`
2. Fill in:
   - GitHub username (e.g. `yourusername`)
   - Repository name (e.g. `khetkart`)
   - Branch: `main`
   - Paste the token from Step 3
   - Choose a simple passcode (so your brother logs in easily next time — this is just a lock on the admin page, on his own device)
3. Click **Save & Connect**. Done!

From here, your brother can add products (title, price, Amazon link, and a photo — either paste a photo link or upload one directly) and they'll appear on the live site within a few seconds.

---

## Notes

- **Where do product photos come from?** He can either paste a link to any image online, or use the "Upload a photo" tab to upload a screenshot straight from the admin page — no separate image hosting needed.
- **Advertisements** work the same way — add text, a link, and an optional small image from the "Advertise on the site" section in admin.
- **Is this secure?** The passcode is a simple convenience lock for the admin page on your brother's own device — it is not bank-level security. The real protection is the GitHub token, which only your brother has and which is never uploaded anywhere public. Don't share the token or the admin link with anyone else.
- **Changing the site name/colors** — everything is in plain HTML/CSS inside `index.html`, so any web developer (or Claude!) can easily reskin it later.
