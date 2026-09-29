# SMS Super Market Website

A responsive, bilingual (English/Tamil) storefront website for SMS Super Market, Pattinamkathan. The original storefront and map photos are included under `client/public/images/` so they work after downloading or cloning this repository.

## Run the website on your computer

Requirements: Node.js 22 or later and pnpm 10 or later.

```bash
pnpm install
pnpm dev
```

Open the local URL printed in the terminal (usually `http://localhost:3000`). To check the TypeScript project and create a production build:

```bash
pnpm check
pnpm build
```

If pnpm is not installed, install it with `npm install --global pnpm` and then run the commands above.

## Deploy on Vercel

This export includes a root `vercel.json` because the project writes its Vite frontend to `dist/public` (not Vite's usual `dist` folder). After pushing the repository to GitHub, import it into Vercel and use these settings if Vercel does not pick them up automatically:

- Framework preset: **Vite**
- Root directory: repository root (`./`)
- Build command: `pnpm build`
- Output directory: `dist/public`

The config also includes an SPA rewrite for client-side routes. If Vercel still shows **Deployment Not Found**, check that you are opening a current deployment URL on the correct Vercel account/team and that the deployment has not been deleted; that platform error refers to a missing or inaccessible deployment, not necessarily a source-code build error. Share the exact URL/error text and Vercel build log if the problem persists.

## Upload this project to GitHub

1. Sign in to GitHub and create a **new repository**. Choose a name such as `sms-super-market`. Choose **Private** unless you specifically want everyone to be able to see the source and supplied shop photos.
2. Download and extract this ZIP on your computer.
3. Open Terminal (macOS/Linux) or PowerShell (Windows) in the extracted `sms-super-market-github` folder, then run:

```bash
git init
git branch -M main
git add .
git commit -m "Add SMS Super Market website"
git remote add origin https://github.com/YOUR-USERNAME/sms-super-market.git
git push -u origin main
```

Replace `YOUR-USERNAME` with your GitHub username. If you chose a different repository name, update the final part of the URL. GitHub may ask you to sign in or authorize Git on the first push.

## Project layout

- `client/src/pages/Home.tsx` — website content, bilingual copy, and interactions
- `client/src/index.css` — layout, visual design, and animation styles
- `client/public/images/` — storefront and location-map photos
- `package.json` — scripts and dependencies

The images have been switched to local `/images/...` paths in this export, so the source does not rely on the original Manus-hosted media URLs. The Manus-only analytics script was also removed from this GitHub copy.
