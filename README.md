# Shola -- 3D Creator Portfolio

A dark-themed, animated 3D creator / full-stack developer portfolio landing page built with React, TypeScript, Tailwind CSS, and Framer Motion.

## Setup

```bash
npm install
npm run dev
```

Then open the printed local URL in your browser.

## Build for production

```bash
npm run build
npm run preview
```

## Structure

- `src/sections/` -- the five page sections (Hero, Marquee, About, Services, Projects)
- `src/components/` -- reusable pieces (FadeIn, Magnet, AnimatedText, ContactButton, LiveProjectButton)
- `src/index.css` -- global styles, Tailwind directives, and the `.hero-heading` gradient-text class

## Deploying to Vercel

This repo is pre-configured for Vercel (framework preset `vite`, build command `npm run build`, output directory `dist`, SPA rewrite included in `vercel.json`).

**Option A -- CLI**
```bash
npm install -g vercel
vercel        # first deploy, follow the prompts
vercel --prod # promote to production
```

**Option B -- Git integration**
1. Push this project to a GitHub/GitLab/Bitbucket repo.
2. In the Vercel dashboard, click "Add New Project" and import the repo.
3. Vercel auto-detects the Vite framework and the settings in `vercel.json` -- no manual config needed.
4. Click Deploy.

No environment variables are required for this project.

## Notes

- Images are pulled from the original hosted URLs (figma.site, motionsites.ai, higgs.ai/cloudfront). Swap in your own asset URLs in `src/sections/*.tsx` when you're ready to replace placeholder art.
- The hero portrait uses a custom `Magnet` component for a mouse-following magnetic hover effect.
- The About section paragraph animates character-by-character as you scroll, via `AnimatedText`.
- The Projects section uses Framer Motion's `useScroll`/`useTransform` to create a sticky, scale-down card-stacking effect.
