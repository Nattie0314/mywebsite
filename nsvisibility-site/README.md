# NS Visibility website

Static one-page site for nsvisibility.com. Hosted free on GitHub Pages.

## Files
- index.html : the whole site (text, styles, layout)
- assets/ : logos and favicon
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
