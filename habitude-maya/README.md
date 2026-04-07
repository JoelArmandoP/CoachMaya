# habitude Maya — Deployment Guide

## What's in this package

```
api/
  chat.js        ← Secure backend (keeps your API key hidden)
public/
  index.html     ← The full Maya coaching app
```

---

## Step 1 — Get an Anthropic API key

1. Go to https://console.anthropic.com
2. Sign up or log in
3. Click **API Keys** in the left menu
4. Click **Create Key**, give it a name (e.g. "habitude-maya")
5. Copy the key — you'll need it in Step 3

---

## Step 2 — Deploy to Vercel

1. Go to https://vercel.com and sign up (free — use your GitHub or Google account)
2. Click **Add New → Project**
3. Choose **"Deploy without a Git repository"** (or drag & drop)
4. Upload this entire folder (or drag the zip)

**Alternative (easiest):**
1. Go to https://vercel.com/new
2. Click **"Continue with GitHub"**
3. Create a free GitHub account if you don't have one
4. Create a new repository, upload these files
5. Import the repo in Vercel

---

## Step 3 — Add your API key (important!)

After deploying:

1. In your Vercel project, click **Settings**
2. Click **Environment Variables**
3. Add a new variable:
   - **Name:** `ANTHROPIC_API_KEY`
   - **Value:** your key from Step 1
4. Click **Save**
5. Go to **Deployments** and click **Redeploy** so the key takes effect

---

## Step 4 — Your app is live!

Vercel gives you a URL like `https://habitude-maya.vercel.app`

You can:
- Share this link directly with clients
- Add a custom domain (e.g. `coach.habitude.com`) in Vercel → Settings → Domains
- Embed it in Squarespace with an iframe code block:

```html
<iframe 
  src="https://your-vercel-url.vercel.app" 
  width="100%" 
  height="700px" 
  style="border:none;"
  allow="camera"
></iframe>
```

---

## Costs

- **Vercel hosting:** Free (Hobby plan is plenty for this)
- **Anthropic API:** Pay per use (~$0.003 per conversation message)
  - A typical coaching session ≈ $0.05–0.15
  - Monitor usage at https://console.anthropic.com/usage

---

## Questions?

Come back to Claude and ask — happy to help troubleshoot.
