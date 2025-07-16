# Vercel Deployment Instructions

## 🚀 Quick Overview
This repository contains a static HTML website for QA intern onboarding that can be deployed to Vercel with zero configuration.

## 📁 Project Structure
```
.
├── index.html          # Main onboarding page
├── vercel.json         # Vercel configuration
└── VERCEL_DEPLOYMENT.md # This file
```

## 🛠️ Deployment Methods

### Method 1: GitHub Integration (Recommended)

1. **Push to GitHub** (if not already done):
   ```bash
   git add .
   git commit -m "Add Vercel configuration"
   git push origin main
   ```

2. **Connect to Vercel**:
   - Visit [vercel.com](https://vercel.com)
   - Sign up/login with your GitHub account
   - Click "Add New Project"
   - Import your repository
   - Vercel will auto-detect it as a static site
   - Click "Deploy"

3. **Automatic Deployments**:
   - Every push to `main` branch will trigger a new deployment
   - Pull requests will generate preview deployments

### Method 2: Vercel CLI

1. **Install Vercel CLI**:
   ```bash
   npm i -g vercel
   ```

2. **Login to Vercel**:
   ```bash
   vercel login
   ```

3. **Deploy**:
   ```bash
   vercel
   ```
   - Follow the prompts
   - Choose "No" for framework detection (it's a static site)
   - Accept default settings

4. **Deploy to Production**:
   ```bash
   vercel --prod
   ```

### Method 3: Drag & Drop

1. Visit [vercel.com/new](https://vercel.com/new)
2. Drag your project folder to the deployment area
3. Click "Deploy"

## ⚙️ Configuration Explained

The `vercel.json` file includes:

- **Security Headers**: XSS protection, content sniffing prevention
- **Caching**: Optimized cache headers for static assets
- **Silent Deployment**: Reduces GitHub notification noise

## 🌐 Custom Domain (Optional)

1. In Vercel dashboard, go to your project
2. Navigate to Settings → Domains
3. Add your custom domain
4. Configure DNS as instructed by Vercel

## 📊 Environment Variables

This static site doesn't require environment variables, but if you need them later:

1. Go to Project Settings → Environment Variables
2. Add variables for different environments (Development, Preview, Production)

## 🔧 Updating the Site

### For GitHub Integration:
```bash
# Make your changes to index.html
git add .
git commit -m "Update onboarding content"
git push origin main
# Vercel will automatically deploy
```

### For CLI Deployment:
```bash
# Make your changes
vercel --prod
```

## 📝 Common Commands

```bash
# Check deployment status
vercel ls

# View deployment logs
vercel logs [deployment-url]

# Remove a deployment
vercel rm [deployment-name]

# Open project in browser
vercel open
```

## 🐛 Troubleshooting

### Common Issues:

1. **Build Fails**: Check that `index.html` is in the root directory
2. **404 Errors**: Ensure your main file is named `index.html`
3. **Slow Loading**: Add appropriate cache headers (already configured)

### Support:
- [Vercel Documentation](https://vercel.com/docs)
- [Vercel Discord](https://vercel.com/discord)
- [GitHub Issues](https://github.com/vercel/vercel/issues)

## 🎯 Next Steps

After deployment:

1. **Test the live site** thoroughly
2. **Share the URL** with your team
3. **Set up monitoring** if needed
4. **Consider adding analytics** (Google Analytics, Vercel Analytics)

## 🔗 Useful Links

- **Vercel Dashboard**: [vercel.com/dashboard](https://vercel.com/dashboard)
- **Static Site Guide**: [vercel.com/docs/concepts/projects/overview](https://vercel.com/docs/concepts/projects/overview)
- **Custom Domains**: [vercel.com/docs/concepts/projects/custom-domains](https://vercel.com/docs/concepts/projects/custom-domains)

---

**Your site will be available at**: `https://[project-name].vercel.app`

🎉 **Happy Deploying!**