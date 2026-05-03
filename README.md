# TRT Management – Rental Landing Page
**7542 Oakland Ave, Kansas City, MO | Available October 1, 2026**

A professional, self-contained rental listing and applicant screening page built for TRT Management. No frameworks, no build tools, no server required — just one HTML file that runs anywhere.

---

## What This Page Does

- Showcases the property with a 27-photo interactive gallery
- Displays rent, availability date, and key property highlights
- Walks prospective renters through a 6-step screening questionnaire
- Automatically disqualifies applicants who don't meet basic requirements
- Prompts qualified applicants to pay the **$35 non-refundable application fee**
- Collects contact information for follow-up

---

## File Structure

```
trt-management-rental/
├── index.html       ← The entire site (rename trt-management-landing.html → index.html)
└── README.md        ← This file
```

> Everything — all photos, styles, and logic — is embedded inside `index.html`. No external dependencies needed.

---

## How to Upload to GitHub & Go Live (Step by Step)

### Step 1 — Create a GitHub Account (if you don't have one)
1. Go to [https://github.com](https://github.com)
2. Click **Sign up** and create a free account
3. Verify your email address

---

### Step 2 — Create a New Repository
1. Once logged in, click the **+** icon in the top-right corner
2. Select **New repository**
3. Fill in the details:
   - **Repository name:** `trt-management-rental` *(or any name you like)*
   - **Description:** `TRT Management rental listing – 7542 Oakland Ave`
   - Set visibility to **Public** *(required for free GitHub Pages hosting)*
   - Check **"Add a README file"**
4. Click **Create repository**

---

### Step 3 — Upload Your Files
1. Inside your new repository, click **Add file → Upload files**
2. Drag and drop (or browse to select) these two files:
   - `index.html` *(rename your downloaded file from `trt-management-landing.html` to `index.html` first)*
   - `README.md` *(this file)*
3. Scroll down and click **Commit changes**

---

### Step 4 — Enable GitHub Pages (Free Hosting)
1. In your repository, click **Settings** (top menu)
2. Scroll down the left sidebar and click **Pages**
3. Under **Branch**, select `main` from the dropdown
4. Leave the folder set to `/ (root)`
5. Click **Save**
6. Wait about 60–90 seconds, then refresh the page
7. GitHub will show you a green banner with your live URL:

```
https://YOUR-USERNAME.github.io/trt-management-rental/
```

That's your live rental page — ready to share!

---

### Step 5 — Share Your Link
Copy your GitHub Pages URL and share it via:
- Text message to prospective renters
- Email
- Social media posts
- Craigslist or Facebook Marketplace listing

---

## How to Add the $35 Application Payment (Stripe)

Right now the **"Pay $35 & Submit"** button shows a success message but doesn't process a real payment. To collect actual payments:

### Option A — Stripe Payment Link (Easiest, No Code)
1. Go to [https://dashboard.stripe.com](https://dashboard.stripe.com) and create a free account
2. In the Stripe dashboard, go to **Payment Links → Create payment link**
3. Add a product called **"Rental Application Fee"** priced at **$35.00**
4. Copy the payment link Stripe gives you (looks like `https://buy.stripe.com/...`)
5. Open `index.html` in a text editor (Notepad, TextEdit, or VS Code)
6. Find this line:
   ```javascript
   function submitPayment() {
   ```
7. Replace the line below it that says `document.getElementById('payment-section')...` with:
   ```javascript
   window.open('https://buy.stripe.com/YOUR_LINK_HERE', '_blank');
   ```
8. Save the file and re-upload it to GitHub (repeat Step 3)

### Option B — Square
Same process, but use [https://squareup.com/us/en/online-checkout](https://squareup.com/us/en/online-checkout) to generate your payment link.

---

## Updating the Page

To make changes (new photos, updated rent, new availability date):

1. Download the latest `index.html` from your repository
2. Make edits in a text editor or contact **Carla Bee** at [info@carlabee.com](mailto:info@carlabee.com) for updates
3. Re-upload the updated file to GitHub (it will automatically replace the old one)
4. Your live site updates within a minute or two

---

## Contact

**TRT Management**
📧 [info@carlabee.com](mailto:info@carlabee.com)
📍 7542 Oakland Ave, Kansas City, MO

*Page designed by Carla Bee – Artistic Image LLC*

---

## Tech Notes

| Feature | How It's Built |
|---|---|
| Photo gallery | Vanilla JavaScript, base64-embedded images |
| Screening form | Multi-step JS with disqualification logic |
| Payment section | Placeholder — wire to Stripe or Square link |
| Hosting | GitHub Pages (free static hosting) |
| Dependencies | None — fully self-contained HTML file |
| Browser support | All modern browsers + mobile |
