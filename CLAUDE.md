# edcuba.com

Static one-page site: `index.html`, `style.css`, `favicon.svg`, plus `terms.txt`, `ai.txt`, `robots.txt`.
`README.md` is the GitHub profile README, hand-edited by the owner. It is not part of the site and not deployed. Don't rewrite it unless asked.

## Design rules
- One font (IBM Plex Mono via Google Fonts), one size (16px), everything centred.
- All lowercase except the name, "Eduard Cuba".
- Two colours mirrored between themes: light `#ece4d6` bg / `#161718` ink, dark the reverse. One muted tone, one red accent.
- Sections are separated by a swaying `~`, header and footer by blinking `· · · ·`. Tagline is `< ai engineer >`.
- CV lines follow "what at where", with the place linked: `genai at google`, `msc in ai at uni zürich`. Most recent first.
- Must fit on one line at phone width (~37 characters).
- Footer: `terms · agents` → `/terms.txt`, `/ai.txt`.

## When changing things
- **Cache:** Cloudflare caches `style.css` and `favicon.svg` at the edge. Bump the `?v=N` on their links in `index.html` whenever either file changes. HTML isn't cached.
- **Privacy:** `terms.txt` lists every third party a visit touches (Cloudflare hosting, Cloudflare Web Analytics, Google Fonts). Update it if you add or remove one, and bump its "Last updated".
- **Analytics:** Cloudflare Web Analytics is injected automatically at the edge. There's no analytics code in the repo; don't add Google Analytics back.
- **robots.txt:** the Content-Signal and AI-crawler rules referenced by `ai.txt` come from Cloudflare's managed robots.txt, which is prepended to this file. The repo copy only adds the `AI-Policy` line.
- **Deploy:** copy the site files (not README/CLAUDE.md) to the server webroot, then check the live page.
