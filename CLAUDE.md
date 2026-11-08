# Portfolio — notes for Claude Code

Static personal portfolio for Sabir Mehdikhanli (SOC Analyst / Blue Team), deployed on Netlify at sabirmehdikhanli.me.

## Structure
- `index.html` — whole site: inline CSS + JS, no framework, no build step
- `_headers` — Netlify security headers (keep the CSP in sync if you add any external script/font/host)
- `robots.txt`

## Rules
- Keep it one self-contained file unless asked otherwise.
- Site content is in English. Talk to Sabir in Azerbaijani.
- Design: dark "SOC" theme — bg #070b10, accents #3ee6a8 / #3aa8ff, fonts Space Grotesk + JetBrains Mono.
- No personal photo, no phone number, no birth date on the site.
- Certificates must link to their official verification URLs (never LinkedIn redirect links).
- The contact form is Netlify Forms (`name="contact"`, `data-netlify="true"`, hidden `form-name`, `bot-field` honeypot). Don't break these attributes.
- Escape any user-provided text before inserting into HTML.
