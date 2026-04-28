# Saleem Furniture & Interiors — Website

## Files
- `index.html` — Home page
- `about.html` — About Us page
- `contact.html` — Contact page
- `style.css` — All styles
- `script.js` — JavaScript (nav, animations, form)
- `logo.svg` — Brand logo (replace with your actual logo file)

---

## Deployment: GitHub Pages

### Option A — GitHub Pages (Free via GitHub Student Pack)

1. Create a GitHub account at https://github.com
2. Create a new **public** repository named exactly:
   `saleemfurnituresinterior.github.io`
   *(or any name if using a custom domain)*

3. Upload all files in this folder to the repository root.

4. Go to **Settings → Pages** → Source: `Deploy from branch` → Branch: `main` → Folder: `/ (root)` → Save.

5. Your site will be live at:
   `https://saleemfurnituresinterior.github.io`

---

## Connecting Your Namecheap Domain

Once your site is live on GitHub Pages:

### Step 1 — GitHub Settings
- Go to **Settings → Pages → Custom domain**
- Enter: `saleemfurnituresinterior.com` (or your exact domain)
- Check "Enforce HTTPS" ✅

### Step 2 — Namecheap DNS Settings
Log into Namecheap → Manage Domain → Advanced DNS → Add these records:

| Type  | Host | Value                  |
|-------|------|------------------------|
| A     | @    | 185.199.108.153        |
| A     | @    | 185.199.109.153        |
| A     | @    | 185.199.110.153        |
| A     | @    | 185.199.111.153        |
| CNAME | www  | saleemfurnituresinterior.github.io |

Wait 24-48 hours for DNS to propagate.

---

## Optional: Azure Static Web Apps (from Student Pack)

1. Push your files to GitHub.
2. Go to Azure Portal → Create **Static Web App**
3. Connect your GitHub repo.
4. Build preset: **Custom** (no framework needed)
5. App location: `/`
6. Output location: leave blank
7. Deploy — Azure auto-deploys on every git push.

---

## Replacing the Logo

Replace `logo.svg` with your actual logo file (PNG or SVG).
If using PNG, update these lines in all 3 HTML files:
```html
<img src="logo.svg" → <img src="your-logo.png"
```

## Contact Form (Make It Actually Send)

The current form simulates sending. To make it real:

**Option 1 — Formspree (free, no backend needed)**
1. Sign up at https://formspree.io
2. Create a form → get your form ID
3. Update the form tag in `contact.html`:
   ```html
   <form class="contact-form" action="https://formspree.io/f/YOUR_ID" method="POST">
   ```
4. Remove the `id="contactForm"` submit handler from `script.js`

**Option 2 — EmailJS (send directly from browser)**
See: https://www.emailjs.com
