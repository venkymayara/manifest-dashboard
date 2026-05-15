# 🚀 MANIFEST App — GitHub Pages + Google Analytics Setup Guide

Get your app live with real multi-user analytics in about 5 minutes.

---

## PART 1 — Publish on GitHub Pages (free hosting)

### Step 1 — Create a GitHub account
Go to **github.com** and sign up (free). Skip if you already have one.

---

### Step 2 — Create a new repository
1. Click the **+** icon (top-right) → **New repository**
2. Name it: `manifest-app` (or anything you like)
3. Set it to **Public** ✅
4. Click **Create repository**

---

### Step 3 — Upload your file
1. On the new repo page, click **uploading an existing file**
2. Drag and drop `index.html` from your computer
3. Scroll down → click **Commit changes**

---

### Step 4 — Enable GitHub Pages
1. In your repo, click **Settings** (top tab)
2. Scroll down to **Pages** (left sidebar)
3. Under **Source**, select **Deploy from a branch**
4. Branch: `main` | Folder: `/ (root)` → click **Save**

⏳ Wait ~60 seconds, then refresh. Your site will be live at:
```
https://YOUR-USERNAME.github.io/manifest-app/
```

---

## PART 2 — Add Google Analytics (free, real multi-user data)

### Step 5 — Create a Google Analytics account
1. Go to **analytics.google.com**
2. Sign in with your Google account
3. Click **Start measuring**
4. Account name: `Manifest App` → Next
5. Property name: `Manifest App` → Next
6. Choose your business type → Next
7. Click **Create** → Accept terms

---

### Step 6 — Set up a Web data stream
1. Choose **Web**
2. Website URL: paste your GitHub Pages URL (e.g. `https://yourname.github.io/manifest-app/`)
3. Stream name: `Manifest Web`
4. Click **Create stream**

---

### Step 7 — Copy your Measurement ID
After creating, you'll see your **Measurement ID** — it looks like:
```
G-XXXXXXXXXX
```
Copy it. You'll need it in the next step.

---

### Step 8 — Update index.html with your real ID
Open `index.html` in a text editor (Notepad, VS Code, etc.).

Find these two lines (near the top of the file):
```html
<script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
```
and:
```javascript
gtag('config', 'G-XXXXXXXXXX');
```

Replace **both** `G-XXXXXXXXXX` with your real Measurement ID. Example:
```javascript
gtag('config', 'G-AB12CD34EF');
```

Save the file.

---

### Step 9 — Re-upload the updated file to GitHub
1. Go to your GitHub repo
2. Click on `index.html`
3. Click the **pencil icon** (Edit) — OR — drag the new file to replace it
4. Click **Commit changes**

GitHub Pages auto-deploys within ~30 seconds.

---

## PART 3 — View your analytics

### What you'll see in Google Analytics:
| Report | Where to find it |
|--------|-----------------|
| Live visitors right now | Reports → Realtime |
| Total users & sessions | Reports → Overview |
| Which tabs people click | Reports → Events |
| Countries & devices | Reports → Demographics |
| Traffic over time | Reports → Acquisition |

### Events already tracked in the app:
- `page_view` — every visit
- `tab_click` — which section was opened (with tab name)
- `goal_added` — when a goal is created
- `affirmation_clicked` — next/prev affirmation
- `gratitude_saved` — journal entry saved
- `vision_item_added` — vision board item added

---

## PART 4 — Share your app

Your live URL is:
```
https://YOUR-USERNAME.github.io/manifest-app/
```

Share it anywhere — it works on mobile and desktop. Every visit is tracked automatically.

---

## FAQ

**Q: Will my localStorage data (goals, affirmations etc.) still work?**
Yes — all personal data is still saved in each user's own browser. GA only tracks aggregate usage.

**Q: Is Google Analytics free?**
Yes, completely free for standard use (up to 10M events/month).

**Q: How long until analytics data shows up?**
Realtime data appears within seconds. Historical reports take up to 24–48 hours to populate.

**Q: Can I use a custom domain (e.g. manifest.maya.com)?**
Yes — GitHub Pages supports custom domains for free. Go to Settings → Pages → Custom domain.

**Q: How do I access the admin panel?**
Tap the MANIFEST logo 5 times quickly. Password: `MAYA2025`

---

*Built with React (CDN) · Hosted on GitHub Pages · Analytics by Google*
