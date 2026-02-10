---
description: How to deploy the Care n Cure Acupuncture Clinic website
---

# Deploying the Website

This project is built with **Vite**, which creates a optimized static site. You can deploy it to any static hosting service like Vercel, Netlify, or GitHub Pages.

## 1. Create a Production Build

First, you need to generate the production files. These are optimized, minified files ready for the public.

1. Open your terminal.
2. Run the build command:
   ```bash
   npm run build
   ```
3. This will create a `dist` folder in your project directory. This folder contains everything you need to deploy.

## 2. Deploy to a Hosting Provider

### Option A: Vercel (Recommended for Easiest Setup)
1. Go to [Vercel.com](https://vercel.com/signup) and sign up.
2. Install Vercel CLI (optional) or just use the dashboard:
   - **Dashboard**: "Import Project" -> Select your GitHub repository -> Vercel usually auto-detects Vite settings. Click "Deploy".
   - **CLI**: Run `npx vercel` in your project folder and follow the prompts.

### Option B: Netlify (Drag & Drop)
1. Run `npm run build` (if you haven't already).
2. Go to [Netlify Drop](https://app.netlify.com/drop).
3. Drag and drop the `dist` folder onto the page.
4. Your site will extend to a live URL immediately.

### Option C: GitHub Pages
1. Push your code to a GitHub repository.
2. Go to Settings -> Pages.
3. Select "GitHub Actions" as the source and use the "Static HTML" workflow, OR use a custom workflow to build Vite.
   *(Since this is a Vite app, simply creating a `gh-pages` branch with the contents of `dist` is the manual way, but using a GitHub Action is better).*

## 3. Verify
Once deployed, check your new URL on mobile and desktop to ensure everything looks perfect!
