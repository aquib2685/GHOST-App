# GHOST App - Deployment Guide

Deploy your GHOST App to the web with these simple guides.

## Deploy to Vercel (Recommended)

Vercel is the easiest and fastest way to deploy React apps.

### Steps:

1. **Push to GitHub** (if not already done):
```bash
git push origin main
```

2. **Sign up at Vercel**: Go to [vercel.com](https://vercel.com) and sign in with GitHub

3. **Import Project**:
   - Click "New Project"
   - Select your `GHOST-App` repository
   - Click "Import"

4. **Configure**:
   - Framework: React
   - Build Command: `npm run build`
   - Output Directory: `build`
   - Leave Environment Variables empty

5. **Deploy**: Click "Deploy" and wait for completion

Your app will be live at a URL like: `https://ghost-app-xxx.vercel.app`

## Deploy to Netlify

1. **Sign up at Netlify**: Go to [netlify.com](https://netlify.com)

2. **Connect Repository**:
   - Click "New site from Git"
   - Select GitHub
   - Choose `GHOST-App` repository

3. **Configure Build Settings**:
   - Build Command: `npm run build`
   - Publish Directory: `build`

4. **Deploy**: Click "Deploy site"

## Deploy to GitHub Pages

1. **Update `package.json`** - Add homepage field:
```json
{
  "homepage": "https://yourusername.github.io/GHOST-App",
  ...
}
```

2. **Install gh-pages**:
```bash
npm install --save-dev gh-pages
```

3. **Add deploy scripts** to `package.json`:
```json
"scripts": {
  "predeploy": "npm run build",
  "deploy": "gh-pages -d build",
  ...
}
```

4. **Deploy**:
```bash
npm run deploy
```

Your app will be at: `https://yourusername.github.io/GHOST-App`

## Deploy to Heroku

1. **Install Heroku CLI**: Download from [heroku.com](https://heroku.com/cli)

2. **Login**:
```bash
heroku login
```

3. **Create app**:
```bash
heroku create your-ghost-app
```

4. **Deploy**:
```bash
git push heroku main
```

## Environment Variables

GHOST App doesn't require any backend environment variables since it uses local storage.

If you add a backend in the future, add them in:
- **Vercel**: Project Settings → Environment Variables
- **Netlify**: Site Settings → Build & Deploy → Environment
- **Heroku**: Settings → Config Vars

## Custom Domain

All hosting platforms allow custom domains:

1. **Purchase a domain** (Namecheap, GoDaddy, etc.)
2. **Update DNS records** to point to your hosting platform
3. **Configure** in your hosting platform's settings

## Performance Tips

- The app uses local storage - no backend needed
- All data stays in the user's browser
- Middleware for caching is optional
- Minimal bundle size (~100KB gzipped)

## Troubleshooting

### Build fails
- Ensure Node.js v14+ is installed
- Run `npm install` to get all dependencies
- Check for console errors

### App not displaying correctly
- Clear browser cache
- Check that all CSS is loading
- Verify JavaScript is enabled

### Messages not persisting
- Local storage is browser-specific
- Messages won't sync across devices
- This is intentional for privacy

## Support

For deployment issues, check:
- Official hosting documentation
- GitHub Issues in this repository
- Community forums for the hosting platform

---

**Happy deploying! 🚀**
