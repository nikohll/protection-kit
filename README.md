# The Protection Strategy Kit · Landing Page

Live the page. Sell the kit. Pay your bills.

---

## What's already done

The page is fully built and ready to ship. All your real images are in place.

```
protection-kit/
├── index.html           ← The landing page (ready)
├── thanks.html          ← Post-purchase delivery page (ready)
├── README.md            ← This file
└── assets/
    ├── logo.png                  ← Your WAL shield logo (in)
    ├── cover.png                 ← Your 2-Book Set image (in)
    ├── nikohl-portrait.jpg       ← Your lifestyle photo (in)
    ├── nikohl-headshot.png       ← Your close-up cut-out, bonus, not currently on the page
    ├── what-every-parent-needs-to-know.pdf   ← YOU NEED TO ADD THIS
    └── crisis-cost-snapshot.pdf              ← YOU NEED TO ADD THIS
```

## Two things you need before you go live

### 1. Drop your two ebook PDFs into the `assets/` folder

Save them with these exact filenames so the thanks page can find them:

- `what-every-parent-needs-to-know.pdf`
- `crisis-cost-snapshot.pdf`

### 2. Create your Stripe Payment Link and paste it into `index.html`

Go to dashboard.stripe.com. Make a product called The Protection Strategy Kit. Price it at $27. Click Create Payment Link. Set the after-payment redirect to your thanks page URL (you'll have that URL after you push to GitHub in step 4 below).

Then open `index.html` in any text editor. Search for `REPLACE_WITH_YOUR_STRIPE_PAYMENT_LINK` and replace it. It appears 3 times. Replace all 3.

---

## Push to GitHub (web browser, no command line needed)

### Step 1: Sign in or create a GitHub account
Go to **github.com**. Sign up if you don't have one. It's free.

### Step 2: Create a new repository
- Click the green **New** button (top left after you sign in)
- Repository name: `protection-kit`
- Set it to **Public**
- Click **Create repository**

### Step 3: Upload all your files
- On the empty repo page, click **uploading an existing file**
- Drag and drop everything from your `protection-kit` folder INTO the browser
  - The two HTML files
  - The README.md
  - The whole `assets/` folder
- Scroll down, click **Commit changes**

### Step 4: Turn on GitHub Pages
- Click **Settings** (top of the repo)
- Click **Pages** in the left sidebar
- Under "Build and deployment":
  - Source: **Deploy from a branch**
  - Branch: **main** → **/ (root)** → **Save**
- Wait 1-2 minutes
- GitHub will show your live URL at the top, something like:
  `https://YOUR-USERNAME.github.io/protection-kit/`

That's your landing page URL. Open it on your phone.

### Step 5: Update Stripe with your real thanks-page URL
Now that you have your real URL, go back to Stripe → your payment link → edit the redirect URL to:
`https://YOUR-USERNAME.github.io/protection-kit/thanks.html`

Save.

### Step 6: Test the whole flow
- Open your landing page on your phone
- Click "Get Instant Access"
- Pay $27 (use a real card, you can refund yourself in Stripe afterward)
- Confirm you land on the thanks page
- Confirm both PDFs download

If anything breaks, fix it before going live on TikTok.

---

## Custom URL for TikTok (optional but better)

The github.io URL is long. Two ways to get a shorter one:

**Quickest:** Put the github.io URL in your TikTok bio. On Live, say "tap my profile, link in bio."

**Better:** If you own wellnessalignedliving.com, you can point a subdomain at your GitHub Pages site. In GoDaddy, add a CNAME record with host `kit` pointing to `YOUR-USERNAME.github.io`. In your GitHub repo Settings → Pages → Custom domain, type `kit.wellnessalignedliving.com`. DNS takes about an hour. Then your URL is `kit.wellnessalignedliving.com`, easy to say on Live.

---

## When you go Live on TikTok

Pin a comment with your URL the second you go on. Repeat the offer every 5-10 minutes since new viewers join constantly. Read Reign's $55,080 story aloud. Read Simone's $88,970 story aloud. Tell people to comment KIT and you'll send them the link in chat. Always anchor the price: "Normally forty-seven, today twenty-seven, two books, instant download."

---

## If you need to update something later

GitHub lets you edit files directly in the browser. Click any file in the repo, click the pencil icon, edit, click Commit changes. Your live page updates within a minute.

---

## If something breaks

| Problem | Fix |
|---|---|
| Photos or logo don't show | Check the file in `assets/` matches the exact filename in the table above |
| PDFs don't download from thanks page | Same: filenames must match exactly |
| Buy button does nothing | Stripe link wasn't pasted in. Search index.html for `REPLACE_WITH` |
| Page looks weird after edits | Hard refresh (Ctrl+Shift+R or Cmd+Shift+R), browser is caching |
| Sale went through but customer got no PDFs | Email them the files manually, then check your thanks.html and assets folder |

Email yourself a copy of every PDF you have on the site so you have a manual backup if a buyer ever has trouble downloading.

---

You've got this.
