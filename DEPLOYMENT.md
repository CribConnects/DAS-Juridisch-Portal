# 🚀 Deployment Guide - DAS Juridisch Portal

## Quick Deploy to Railway

### Prerequisites
- GitHub account
- Railway account (sign up at [railway.app](https://railway.app))
- Git installed locally

### Step-by-Step Deployment

#### 1. Push to GitHub ✅

The code is already on the branch `claude/create-das-portal-43pdQ`. Just push any final changes:

```bash
git add .
git commit -m "Ready for Railway deployment"
git push -u origin claude/create-das-portal-43pdQ
```

#### 2. Deploy on Railway 🚂

**Option A: Using Railway Dashboard**

1. Go to [railway.app](https://railway.app) and sign in
2. Click **"New Project"**
3. Select **"Deploy from GitHub repo"**
4. Authorize Railway to access your GitHub account if needed
5. Select repository: **`CribConnects/DAS-Juridisch-Portal`**
6. Select branch: **`claude/create-das-portal-43pdQ`**
7. Railway will automatically:
   - Detect Node.js
   - Install dependencies
   - Start the server
8. Click **"Deploy"**

**Option B: Using Railway CLI**

```bash
# Install Railway CLI
npm i -g @railway/cli

# Login to Railway
railway login

# Initialize project
railway init

# Deploy
railway up
```

#### 3. Get Your URL 🌐

1. Go to your Railway project dashboard
2. Click on your service
3. Go to **"Settings"** tab
4. Under **"Domains"** section:
   - Click **"Generate Domain"** for a free railway.app subdomain
   - OR click **"Custom Domain"** to add your own domain

Your portal will be live at: `https://your-project-name.up.railway.app`

#### 4. Configure Environment (Optional) ⚙️

Railway automatically sets:
- `PORT` - The port your app runs on
- `NODE_ENV` - Set to "production"

No additional configuration needed!

### Verification Checklist ✓

After deployment, verify:

- [ ] Home page loads correctly
- [ ] Navigation between sections works
- [ ] File upload interface is functional
- [ ] Chat interface is responsive
- [ ] HeyGen video avatar loads (check browser console for any errors)
- [ ] Responsive design works on mobile

### Custom Domain Setup (Optional)

1. In Railway dashboard, go to Settings > Domains
2. Click "Custom Domain"
3. Enter your domain (e.g., `portal.das.nl`)
4. Add the provided DNS records to your domain provider:
   - Type: `CNAME`
   - Name: `portal` (or your subdomain)
   - Value: `your-project.up.railway.app`
5. Wait for DNS propagation (usually 5-60 minutes)

### Monitoring & Logs

**View Logs:**
1. Railway Dashboard > Your Project
2. Click "View Logs"
3. Real-time logs will appear

**Metrics:**
- CPU usage
- Memory usage
- Network traffic
- Deployment history

### Troubleshooting 🔧

**Issue: Port binding error**
- Solution: Railway automatically sets PORT variable, no action needed

**Issue: Module not found**
- Solution: Ensure package.json is in root directory
- Run: `railway run npm install`

**Issue: HeyGen avatar not loading**
- Check browser console for errors
- Verify HeyGen API key is valid
- Check if microphone permissions are granted

**Issue: 404 errors**
- Ensure index.html is in root directory
- Check server.js routing configuration

### Updating Your Deployment

To deploy updates:

```bash
# Make your changes
git add .
git commit -m "Update: description of changes"
git push origin claude/create-das-portal-43pdQ
```

Railway will automatically redeploy! 🎉

### Cost Estimation 💰

Railway offers:
- **Free Tier**: $5 credit/month (enough for small apps)
- **Developer Plan**: $5/month + usage
- **Team Plan**: $20/month + usage

This portal typically uses:
- ~0.5GB RAM
- ~100MB storage
- Minimal CPU (static site)

**Expected cost**: Free tier should be sufficient!

### Environment Variables (if needed)

Add in Railway Dashboard > Settings > Variables:

```
NODE_ENV=production
PORT=(automatically set)
```

### Security Best Practices 🔒

1. **HTTPS**: Automatically enabled by Railway ✓
2. **Environment Variables**: Use Railway's secrets for sensitive data
3. **CORS**: Configure in server.js if needed
4. **Rate Limiting**: Consider adding for production

### Support & Resources

- **Railway Docs**: https://docs.railway.app
- **Railway Community**: https://discord.gg/railway
- **GitHub Issues**: Report problems in the repository
- **DAS Support**: support@das.nl

---

## Alternative Deployment Options

### Vercel
```bash
npm i -g vercel
vercel
```

### Netlify
```bash
npm i -g netlify-cli
netlify deploy --prod
```

### Heroku
```bash
heroku create das-juridisch-portal
git push heroku claude/create-das-portal-43pdQ:main
```

---

**🎉 Congratulations! Your DAS Juridisch Portal is now live!**

Share your deployment URL and start helping users with legal assistance powered by AI.
