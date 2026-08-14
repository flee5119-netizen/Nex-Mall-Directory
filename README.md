[README.md](https://github.com/user-attachments/files/31050938/README.md)
# NEX Mall Food Directory 🌈

A Care Bears–themed food directory for nex (Serangoon Station), built as a single static
HTML page with a live search bar and Halal filter. No build step, no dependencies —
just plain HTML/CSS/JS in `index.html`.

## 1. Push this to GitHub

From inside this folder:

```bash
git init
git add .
git commit -m "Initial commit: NEX food directory"
git branch -M main
git remote add origin https://github.com/<your-username>/<your-repo-name>.git
git push -u origin main
```

(Create the empty repo on GitHub first at https://github.com/new — don't initialize it
with a README so there's no merge conflict.)

## 2. Deploy to Vercel

**Option A — Vercel dashboard (easiest)**
1. Go to https://vercel.com/new
2. Click "Import Git Repository" and select the repo you just pushed.
3. Framework Preset: choose **"Other"** (it's a static site — no build command needed).
4. Leave Build Command and Output Directory blank.
5. Click **Deploy**. Vercel will serve `index.html` at your project's root URL.

**Option B — Vercel CLI**
```bash
npm i -g vercel
cd nex-food-directory
vercel        # follow prompts, link/create project
vercel --prod # deploy to production
```

## Project structure

```
nex-food-directory/
├── index.html      # the entire app (HTML + CSS + JS, no build needed)
├── vercel.json      # static site config (clean URLs)
└── README.md
```

## Notes

- Stall numbers, phone numbers, and Halal status were verified against the official
  nex.com.sg store directory as of Aug 2026. This covers a curated subset of outlets,
  not the full 90+ F&B list at nex — update `outlets` array in `index.html` to add more.
- "View Menu" buttons link to a Google search for the outlet's menu, since not every
  stall has a confirmed official website.
- "Reserve" buttons (tel: links) only appear for outlets confirmed to be sit-down
  restaurants that take phone bookings.
