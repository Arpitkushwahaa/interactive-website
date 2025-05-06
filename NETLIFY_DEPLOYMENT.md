# Netlify Deployment Guide

This guide walks you through deploying your interactive 3D website to Netlify.

## Option 1: Deploy via Netlify UI (Recommended for Beginners)

### Prerequisites
- Your code pushed to a Git repository (GitHub, GitLab, or Bitbucket)
- A Netlify account (free tier is sufficient)

### Steps

1. **Create a Netlify account**
   - Go to [netlify.com](https://www.netlify.com/) and sign up for an account

2. **Start a new deployment**
   - From your Netlify dashboard, click "Add new site" > "Import an existing project"

3. **Connect to your Git provider**
   - Choose GitHub, GitLab, or Bitbucket
   - Authenticate with your Git provider
   - Select the repository containing your project

4. **Configure build settings**
   - Netlify will automatically detect the correct settings from your netlify.toml file
   - Build command: `npm run build`
   - Publish directory: `dist`

5. **Deploy your site**
   - Click "Deploy site"
   - Netlify will build and deploy your site
   - Once complete, you'll get a unique URL (e.g., `https://your-site-name.netlify.app`)

6. **Set up a custom domain (optional)**
   - In your site settings, navigate to "Domain management"
   - Click "Add custom domain" and follow the instructions

## Option 2: Deploy via Netlify CLI

### Prerequisites
- Node.js and npm installed
- Netlify CLI installed (`npm install netlify-cli -g`)

### Steps

1. **Install Netlify CLI**
   ```bash
   npm install netlify-cli -g
   ```

2. **Login to your Netlify account**
   ```bash
   netlify login
   ```

3. **Initialize your project**
   ```bash
   netlify init
   ```
   - Choose "Create & configure a new site"
   - Select your Netlify team
   - Provide a name for your site (optional)

4. **Deploy your site**
   ```bash
   netlify deploy --prod
   ```
   - This will build your project and deploy it to Netlify
   - After deployment, you'll receive your live site URL

## Continuous Deployment

Once you've set up your site on Netlify, any pushes to your repository's main branch will automatically trigger a new deployment. This ensures your site is always up to date with your latest code.

## Environment Variables (If Needed)

If your project uses environment variables:
1. Go to Site settings > Build & deploy > Environment
2. Add your environment variables there

## Advanced Features

Netlify offers many advanced features:
- Custom domains with free SSL certificates
- Form handling
- Authentication
- Serverless functions
- Split testing

Visit the [Netlify Docs](https://docs.netlify.com/) to learn more about these features.

## Troubleshooting

### Issue: Build fails
- Check your build logs in Netlify for specific errors
- Ensure all dependencies are properly listed in package.json
- Make sure your build command is correctly set to `npm run build`

### Issue: Site deploys but doesn't load correctly
- Check if your site uses correct base paths for assets
- Ensure the netlify.toml file has the correct redirects setup

### Issue: Routes don't work on refresh
- The redirects in netlify.toml should handle this, but verify they're correct
- All routing should redirect to index.html to support client-side routing

For more help, consult the [Netlify Support Forums](https://answers.netlify.com/) or [Netlify Documentation](https://docs.netlify.com/). 