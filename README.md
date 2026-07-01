# Swavant static site (staging)

Static marketing site for Swavant, no build step required. Every page is a
single self-contained HTML file (CSS and images are inlined), so this can be
served as-is by any static host, including Cloudflare Pages.

## Staging notes

- Every page has `<meta name="robots" content="noindex, nofollow">` and a
  "Staging preview" badge, since this is for private review, not launch.
- Stats, brand logos, and case studies on the home and results pages are
  placeholders (`[creator count]`, `[Brand name]`, etc.) pending real numbers.
- Login, signup, and dashboard mockup pages exist in this repo
  (`login.html`, `signup.html`, `dashboard-*.html`) but are intentionally not
  linked from navigation or the footer, so reviewers only see the marketing
  pages: `index`, `services`, `talent`, `results`, `creators`, `brands`,
  `about`, `apply`, `contact`.

## Deploying to Cloudflare Pages

1. Push this repo to GitHub.
2. In Cloudflare Pages, "Create a project" → "Connect to Git" → select this
   repo.
3. Build settings: no build command, output directory `/` (root). There's
   nothing to build, these are static files.
4. Deploy. Cloudflare gives you a `*.pages.dev` URL to share for feedback.

## Before removing the noindex tag / going live

Swap the placeholder stats and case studies for real numbers, decide whether
to re-enable login/signup/dashboard links, and remove the staging badge and
robots meta tag (or ask for that pass when ready).
