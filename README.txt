bogdin.dev portfolio - how to use this repo

STRUCTURE
- index.html       - the whole site: markup, styles and content in one file.
- assets/work/     - project photos (webp), used in the GROUPS block.
- assets/media/    - extra photos and video for projects (webp/mp4).
- icons/, favicon.ico - tab icon and phone/PWA icons.
- og-image.png     - link preview image (OpenGraph/Twitter).
- Bogdan-Sliusarenko-Mechanical-Engineer.pdf - the file downloaded by the "Download CV" button.
- CNAME            - custom domain for GitHub Pages (bogdin.dev).
- robots.txt, sitemap.xml - for search engine crawlers.
- google*.html     - Google Search Console ownership verification file. DO NOT DELETE, or verification is lost.

EDITING TEXT
All content lives in JS blocks near the end of index.html:
- CONFIG       - name, email, phone, LinkedIn, location.
- T            - all UI copy (buttons, section headings).
- INTRO_PARAS / INTRO_CARDS - the "About myself" text and the three cards below it.
- GROUPS       - projects and photos in the "Work" section (titles, descriptions, photo captions).
- EXPERIENCE   - the experience timeline.
- TESTIMONIALS - quotes in the "Recommendations" section.

The site is single-language (English) - there is no RU/EN toggle.

REPLACING THE CV
Put the new PDF next to index.html, and either:
- name it the same: Bogdan-Sliusarenko-Mechanical-Engineer.pdf, or
- rename it and update the href/download attributes on the "Download CV" link in the contact section.

LOCAL PREVIEW
Open index.html directly in a browser - the site is static, no server needed.

DEPLOYMENT
The site is published automatically via GitHub Pages from
github.com/bogdan770/portfolio, branch main. To publish an update:
  git add <files>
  git commit -m "..."
  git push origin main
Changes go live on https://bogdin.dev/ within a minute or two.
DNS and the domain are managed through Cloudflare.

ANALYTICS
Cloudflare Web Analytics is embedded directly in index.html (a
script tag near the end of <body>). View stats at
dash.cloudflare.com -> Web Analytics.

SEO
- robots.txt allows indexing for all crawlers; sitemap.xml points to
  the single page /.
- <head> includes a canonical link, robots/author meta tags and
  JSON-LD (schema.org Person) for Google's search result card.
- The site is verified in Google Search Console (see google*.html above).

NOT PART OF THE LIVE SITE
The VEEV/ and ss/ folders, Bogdan-Sliusarenko-Portfolio.html and
portfolio-deploy.zip exist locally in this folder but are excluded
from git (.gitignore) - they're drafts/source material, not part of
the deployed site.
