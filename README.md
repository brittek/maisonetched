# Maison Etched

A refined digital presence for a modern Sydney atelier. Elegant, minimal landing page showcasing the Maison Etched brand.

**Live Site:** [www.maisonetched.com](https://www.maisonetched.com)

## Features

- **Responsive Design** – Mobile-first approach with adaptive layouts for all devices
- **Refined Aesthetics** – Minimal, sophisticated design with custom color palette
- **Smooth Animations** – Hardware-accelerated entrance animations for premium feel
- **Grid Texture Background** – Subtle design detail with radial masking
- **Safe Area Support** – Full notch/safe area compatibility for mobile devices
- **HTTPS Protected** – Auto-provisioned SSL certificate via Vercel & GoDaddy

## Technology Stack

- **HTML** – Clean semantic markup
- **CSS** – Tailwind CSS (CDN) with custom theme extensions
- **Typography** – Google Fonts (Cormorant Garamond + Instrument Sans)
- **Hosting** – [Vercel](https://vercel.com)
- **Domain** – GoDaddy DNS management

## Color Palette

| Color | Hex | Usage |
|-------|-----|-------|
| Bone | `#E7E6DE` | Background |
| Burgundy | `#470908` | Accent/Hover |
| Ink | `#1A1A1A` | Text |
| Steel | `rgba(26, 26, 26, 0.04)` | Borders |

## Getting Started

### Local Development

```bash
# Clone the repository
git clone https://github.com/brittek/maisonetched.git
cd maisonetched

# Serve locally (using Python)
python -m http.server 5000
# or using Node.js
npx serve
```

Open `http://localhost:5000` in your browser.

### Project Structure

```
maisonetched/
├── index.html              # Main landing page
├── vercel.json            # Vercel deployment config
├── DEPLOYMENT.md          # Deployment guide
├── README.md              # This file
└── .github/
    └── workflows/
        └── deploy.yml     # GitHub Actions (optional)
```

## Deployment

Hosted on **Vercel** with automatic deployments on every push to `main`.

- **Production URL:** https://www.maisonetched.com
- **Vercel Default:** https://maisonetched.vercel.app
- **DNS Provider:** GoDaddy

For detailed setup instructions, see [DEPLOYMENT.md](DEPLOYMENT.md).

### Deploy Manually

Every push to the `main` branch automatically triggers a new deployment via Vercel. No manual action required.

## Development

**Making Changes:**
1. Edit files locally
2. Test in browser (localhost)
3. Commit and push to `main`
4. Vercel auto-deploys within seconds

**Previews:**
Vercel creates preview deployments for pull requests automatically.

## License

© 2026 Maison Etched. All rights reserved.

---

**Built with ❤️ by [Brittek Digital](https://brittek.com)**
