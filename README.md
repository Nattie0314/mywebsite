# NS Visibility website

Static site for nsvisibility.com. Hosted free on GitHub Pages.

## Files
- index.html : the homepage (text, styles, layout)
- services/index.html : the Services page, served at /services/.
- how-it-works/index.html : the How it works page, served at /how-it-works/.
- about/index.html : the About page, served at /about/.
  Each page has its own copy of the shared styles (header, buttons, footer), so style changes
  there may need making in every page.
- 404.html : branded "page not found" page (GitHub Pages serves it for missing URLs)
- favicon.ico : browser tab icon
- assets/ : logos, photo and icons. The `-640.webp`, `-720.webp` and `-572.webp` files are
  smaller copies of the PNG logos used on the page; the PNGs stay as master files and the
  badge PNG is the social sharing image.
- assets/fonts/ : self-hosted Montserrat (same files Google Fonts serves), with its OFL licence
- CNAME : tells GitHub Pages to serve the site on nsvisibility.com
- robots.txt, sitemap.xml : for search engines

## Deploy
1. Create a public GitHub repo (for example `nsvisibility`).
2. Upload everything in this folder to the repo root (drag and drop works on github.com).
3. Repo Settings, Pages, deploy from the `main` branch, root folder.
4. Under Custom domain enter `nsvisibility.com`.
5. At GoDaddy DNS, delete the old `A` record for `@`, then add four `A` records for `@`:
   185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153
6. Change the `www` CNAME to `YOUR-GITHUB-USERNAME.github.io`.
7. When DNS updates (15 minutes to a few hours), tick Enforce HTTPS in Pages.

## Edit later
- Email address: search for `mailto:` in index.html.
- Text: all copy is plain HTML in index.html.
- After deploying, add the site in Google Search Console and submit sitemap.xml.
- When you add a page, give it its own <title>, meta description and canonical URL,
  and add it to sitemap.xml.
- URL rule: every page URL ends with a trailing slash (`/services/`, never `/services`).
  Create each page as `folder-name/index.html` so GitHub Pages serves it at `/folder-name/`
  and redirects the no-slash version there. Use the trailing-slash URL everywhere: internal
  links, canonical, og:url, structured data and sitemap.xml. Files (images, fonts, favicon)
  keep their normal paths without a slash.
