# Portfolio — notes for Claude Code

Static personal portfolio for Sabir Mehdikhanli (SOC Analyst / Blue Team), deployed on GitHub Pages (repo saabir00/portfolio, branch main, root) at sabirmehdikhanli.me.

## Structure
- `index.html` — whole site: inline CSS + JS, no framework, no build step
- `_headers` — security headers (only applied on Netlify; GitHub Pages ignores this file). Keep the CSP in sync if you add any external host.
- `robots.txt`

## Rules
- Keep it one self-contained file unless asked otherwise.
- Site content is in English. Talk to Sabir in Azerbaijani.
- Design: cinematic minimal dark — near-black bg #0a0a0b, glowing planet-horizon arc with a BLUE glow and blue aurora (Blue Team identity) + twinkling stars in the hero. Inside the hero only (absolute layer, not fixed — so it never scrolls separately on phones), a very faint, transparent SOC log stream (canvas: Sysmon/Windows/Wazuh/Splunk/QRadar-style lines scrolling upward, rare red ALERT and green ACTION lines, masked out around the center so the name stays clean) fades in on load and fades out as the user scrolls past the hero. The earlier purple video background was removed on purpose. Italic serif (Instrument Serif) is used ONLY for the name in the hero; everything else is Inter (headings 600, tight letter-spacing). Glass cards (rgba(255,255,255,.035), 1px rgba(255,255,255,.08) border, 18px radius), light pill buttons, blur-in reveal animations. Accents #7ee0b5 / #89b4ff, used sparingly. Animations, stars (drift + twinkle + mouse parallax) and the log stream run for everyone, including visitors with reduced-motion enabled — this is Sabir's explicit choice, do not re-add prefers-reduced-motion gating.
- No terminal/console section (removed on purpose).
- Logo: original white monoline shield with a continuous angular "SM" ligature inside (inline SVG `<symbol id="logo">` for the nav, animated inline SVG in the hero, also the favicon). Hero animation: S→M ligature draws in, then the shield outline, then a soft permanent glow + light sweep along the shield + very subtle 3D tilt. Do not replace it with stock logo artwork.
- No personal photo, no phone number, no birth date on the site.
- Certificates must link to their official verification URLs (never LinkedIn redirect links).
- Contact form: posts to `/` (Netlify Forms attributes kept); on GitHub Pages this fails and the form falls back to "Open in email / Copy message". Planned: switch the endpoint to Formspree.
- Escape any user-provided text before inserting into HTML.
