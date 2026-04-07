# Deployment Guide: Maison Etched

## Vercel Setup

This site is hosted on Vercel with automatic deployments on push to `main`.

### Step 1: Connect Repository to Vercel

1. Visit https://vercel.com and sign in (or create an account)
2. Click **Add New...** → **Project**
3. Select **Import Git Repository**
4. Search for `maisonetched` and select the repository
5. Click **Import**
6. Leave build settings as default (already configured in `vercel.json`)
7. Click **Deploy**

The site will be live at `maisonetched.vercel.app` automatically.

### Step 2: Add Custom Domain in Vercel

1. In the Vercel project dashboard, go to **Settings** → **Domains**
2. Click **Add Domain**
3. Enter: `www.maisonetched.com`
4. Select **Using GoDaddy** (or your DNS provider)
5. Vercel will show you the DNS records to add

### Step 3: Configure GoDaddy DNS

✅ **CONFIGURED** — Your DNS records are now set:

**Apex Domain (maisonetched.com):**

| Type | Name | Value | TTL |
|------|------|-------|-----|
| A | @ | `76.76.19.131` | 1 hour |
| A | @ | `76.76.19.132` | 1 hour |
| A | @ | `76.76.19.133` | 1 hour |
| A | @ | `76.76.19.134` | 1 hour |

**WWW Subdomain:**

| Type | Name | Value | TTL |
|------|------|-------|-----|
| CNAME | www | `cname.vercel-dns.com.` | 1 hour |

**Email (Office 365):**
- MX records ✓
- SPF, DMARC, Autodiscover ✓
- All email subdomains configured ✓

### Step 4: Verify Domain

1. Return to Vercel's domain settings
2. Wait 5-10 minutes for DNS propagation
3. Vercel will automatically verify and show a green checkmark
4. HTTPS certificate auto-provisions instantly
5. Visit https://www.maisonetched.com

## Deployment Checklist

- [x] Create Vercel account and connect GitHub repository
- [x] Deploy to Vercel (auto on git push)
- [x] Add custom domain `maisonetched.com` in Vercel Settings
- [x] Configure DNS records in GoDaddy (Apex domain + www + email)
- [ ] Wait for DNS propagation (5-10 minutes)
- [ ] Verify domain in Vercel dashboard (green checkmark)
- [ ] Visit https://maisonetched.com and confirm it loads
- [ ] Confirm HTTPS is active (lock icon in browser)

## Automatic Deployments

Every push to `main` automatically deploys to production at https://www.maisonetched.com

**Preview Deployments:** Vercel creates a unique URL for each pull request.

## Troubleshooting

**Domain not connecting?**
- Check DNS propagation: `nslookup www.maisonetched.com`
- Ensure CNAME record is correctly set in GoDaddy
- Wait longer for DNS propagation (up to 48 hours in rare cases)

**Deployment failed?**
- Check Vercel deployment logs in project dashboard
- Ensure `vercel.json` is correctly configured

**HTTPS certificate issues?**
- Certificate auto-provisions after domain is verified
- May take a few minutes after DNS is live
