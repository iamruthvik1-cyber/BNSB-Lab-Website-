# BNSB Lab Website

**Biological Networks and Systems Biology Lab**
Dr. Abhishek Subramanian · Department of Biotechnology · IIT Hyderabad

---

##  Quick Start — Open Locally

Just double-click **`index.html`** — it opens directly in any browser, no server needed.

All CSS, JavaScript, and images are embedded inside `index.html` so it is fully self-contained and works offline.

---

##  Folder Structure

```
bnsb-lab-website/
│
├── index.html                ← THE WEBSITE — open this in any browser
│
├── assets/
│   ├── css/
│   │   └── styles.css        ← Separated CSS (for editing / reference)
│   ├── js/
│   │   └── main.js           ← Separated JS  (for editing / reference)
│   └── images/               ← (Images are embedded in index.html)
│
├── .nojekyll                 ← GitHub Pages: disables Jekyll processing
├── netlify.toml              ← Netlify: one-click deploy config
├── vercel.json               ← Vercel: one-click deploy config
└── README.md                 ← This file
```

> **Note:** `styles.css` and `main.js` are reference copies for editing.
> `index.html` already contains all styles and scripts inline, so it works
> standalone without those files.

---

## 🌐 Deploy Online (Free)

### GitHub Pages — Recommended

1. Create a new repo at [github.com/new](https://github.com/new)
2. Upload all files (keep the folder structure)
3. Go to **Settings → Pages → Source** → `Deploy from a branch` → `main` → `/ (root)` → **Save**
4. Your site is live at `https://<username>.github.io/<repo-name>/`

### Netlify — Drag & Drop

1. Go to [app.netlify.com](https://app.netlify.com) → **Add new site → Deploy manually**
2. Drag the `bnsb-lab-website` folder onto the page
3. Done — live in 30 seconds. Free custom domain available.

### Vercel

1. Go to [vercel.com](https://vercel.com) → **Add New Project**
2. Import from GitHub, or click **"Deploy without Git"** and upload the folder
3. Click **Deploy**

### Any Web Host / cPanel

Upload all files to the `public_html` folder (or `www`) via FTP/SFTP.

---

##  How to Edit Content

### Update a publication

Open `index.html`, find `id="pg-articles"` and add a `<div class="pitem">`:

```html
<div class="pitem" data-cat="iith">
  <div class="pyear">2026</div>
  <div>
    <div class="ptitle">Your Paper Title</div>
    <div class="pauthors">Author A, <strong>Abhishek Subramanian</strong>, Author B</div>
    <div class="pjournal">Journal Name, Vol(Issue), Pages</div>
    <a href="https://doi.org/..." target="_blank" class="pdoi">DOI: ... ↗</a>
  </div>
</div>
```

`data-cat` values: `iith` · `previous` · `patent` · `book`

### Add a team member photo

Find the person's `<div class="tcard">` in the `id="pg-members"` section.
Replace the placeholder with:

```html
<div class="tphoto">
  <img src="data:image/jpeg;base64,..." 
       alt="Name" 
       style="width:100%;height:100%;object-fit:cover;object-position:top center">
</div>
```

To get the base64 string: paste your image at [base64.guru/converter/encode/image](https://base64.guru/converter/encode/image).

### Update contact / email

Search `index.html` for `abhisheks@bt.iith.ac.in` to find all contact references.

### Edit CSS or JS

Edit `assets/css/styles.css` or `assets/js/main.js`, then copy-paste the content
back into `index.html` between the `<style>` and `<script>` tags.

---

##  Pages / Sections

| Section | ID | Description |
|---|---|---|
| Home | `pg-home` | Hero banner, research areas, funding logos |
| Research | `pg-research` | Research overview |
| Projects | `pg-projects` | 4 active research projects |
| Collaborations | `pg-collaborations` | 5 collaborators (India + international) |
| Meet the Team | `pg-team` | Team hub page |
| Group Leader | `pg-leader` | PI bio, achievements, talks, courses |
| Team Members | `pg-members` | PhD scholars, M.Tech students, interns, alumni |
| Research Articles | `pg-articles` | 28 publications with category filter |
| Tools & Databases | `pg-tools` | Lab tools: NAViFluX, MATRIX, etc. |
| Activities | `pg-activities` | Activities hub |
| Events | `pg-events` | Events list |
| Gallery | `pg-gallery` | Photos with category filter tabs |
| Contact | `pg-contact` | Opportunities, contact form info |

---

##  Design System

All colours and spacing live as CSS variables in `assets/css/styles.css` (and inline in `index.html`):

```css
:root {
  --bg:    #f6f9ff;    /* page background */
  --g900:  #0b1f4a;   /* darkest navy (headings) */
  --g700:  #1a56c4;   /* primary blue */
  --g600:  #2970e8;   /* accent blue (links, buttons) */
  --g400:  #5b9bf5;   /* light blue */
  --accent:#2970e8;
  --fa: 'Cormorant Garamond', serif;   /* display font */
  --fb: 'Outfit', sans-serif;          /* body font */
}
```

Fonts are loaded from **Google Fonts** — an internet connection is needed for correct rendering. Fallbacks are `serif` and `sans-serif`.

---

##  Content Summary

| Content | Count |
|---|---|
| Publications (IITH) | 8 |
| Publications (Previous) | 17 |
| Book chapters | 3 |
| Patents | 1 |
| PhD scholars | 5 |
| M.Tech students | 4 |
| Current interns | 2 |
| Collaborators | 5 |
| Research projects | 4 |
| Gallery photos | 9 |

---

##  Contact

Dr. Abhishek Subramanian
Department of Biotechnology, IIT Hyderabad
✉ abhisheks@bt.iith.ac.in
🔗 https://sites.google.com/bt.iith.ac.in/comp-bio-abhishek/

---

*Last updated: June 2026*
