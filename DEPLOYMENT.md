# Deployment Guide

Follow these steps to deploy your website to GitHub Pages:

## 1. Create a GitHub Repository

1. Go to [GitHub](https://github.com/) and sign in to your account
2. Click on the "+" icon in the top-right corner and select "New repository"
3. Name your repository (e.g., "interactive-3d-website")
4. Choose public or private visibility
5. Click "Create repository"

## 2. Initialize and Push Your Code

Run these commands in your project directory:

```bash
# Initialize a git repository
git init

# Add all files to staging
git add .

# Commit your changes
git commit -m "Initial commit"

# Add your GitHub repository as the remote origin
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPOSITORY_NAME.git

# Push your code to GitHub
git push -u origin main
```

Note: If your default branch is named "master" instead of "main", use `git push -u origin master` instead.

## 3. Deploy to GitHub Pages

Once your code is pushed to GitHub, you can deploy using:

```bash
# Build and deploy
npm run deploy
```

This will:
1. Build your project (via the predeploy script)
2. Deploy it to a special branch called "gh-pages"
3. Configure GitHub Pages to serve your site

## 4. Configure GitHub Pages

1. Go to your repository on GitHub
2. Click on "Settings"
3. Select "Pages" from the left sidebar
4. Under "Source", ensure "Deploy from a branch" is selected
5. Choose "gh-pages" branch and "/ (root)" folder
6. Click "Save"

## 5. Access Your Website

After a few minutes, your website will be available at:
`https://YOUR_USERNAME.github.io/YOUR_REPOSITORY_NAME/`

## Troubleshooting

- If your site is missing styles or doesn't load correctly, ensure the `base` property in `vite.config.js` is set to `'./'`
- If images or assets don't load, check the paths in your code (they should be relative)
- For custom domains, you can configure them in the GitHub Pages settings

## Updating Your Site

Make your changes locally, then run:

```bash
npm run deploy
```

This will rebuild and redeploy your site to GitHub Pages. 