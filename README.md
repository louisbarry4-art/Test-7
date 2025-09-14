Automated Affiliate Site (Jekyll + GitHub Pages)


This repo is a starter scaffold for an automated affiliate marketing site. It uses GitHub Pages to host a Jekyll site and a GitHub Actions workflow that fetches a published Google Sheet CSV and converts rows into `_posts/*.md` files.


## Quick setup


1. Create a GitHub repository and paste these files.
2. In the repo Settings -> Pages, enable GitHub Pages using the `main` branch (or let GitHub Pages use the default branch). If you named the repo `username.github.io`, your site will be at `https://username.github.io`.
3. Create a Google Sheet with columns: `title | slug | date | content | affiliate_url | tags` and add your content rows.
4. File -> Publish to web -> publish the sheet as CSV and copy the CSV link.
5. In GitHub: Settings -> Secrets and variables -> Actions -> New repository secret
- Name: `SHEET_CSV_URL`
- Value: the CSV link from step 4
6. Commit and push the repo. In GitHub Actions trigger or wait for the scheduled run to generate `_posts/` from the sheet.


## Notes
- Always include a disclosure on pages with affiliate links; the template includes a disclosure line in generated posts.
- Use `rel="sponsored noopener noreferrer"` on affiliate links to follow best practices.
- Improve SEO by registering the site in Google Search Console and submitting a sitemap.
