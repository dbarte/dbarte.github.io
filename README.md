# Davis Bartels — academic website

A small, dependency-free academic website built for GitHub Pages. It is responsive, supports dark mode, uses no external fonts or analytics, and requires no build step.

## Preview locally

Open `index.html` in a browser. For the most accurate preview, start a local web server in this folder:

```sh
python3 -m http.server 8000
```

Then visit `http://localhost:8000`.

## Publish with GitHub Pages

### Option A: a personal site (cleanest URL)

1. On GitHub, create a repository named `YOUR-USERNAME.github.io`, replacing `YOUR-USERNAME` with your exact GitHub username.
2. Upload every file in this folder to the repository root, including `.nojekyll`.
3. Open the repository's **Settings → Pages**.
4. Under **Build and deployment**, set **Source** to **Deploy from a branch**.
5. Select the `main` branch and `/ (root)`, then save.
6. After GitHub finishes publishing, visit `https://YOUR-USERNAME.github.io`.
7. In **Settings → Pages**, enable **Enforce HTTPS** if it is not already enabled.

### Option B: a project site

Use any repository name. The site URL will be `https://YOUR-USERNAME.github.io/REPOSITORY-NAME/`. All paths in this site are relative, so the site works without edits.

### Command-line upload (optional)

After creating an empty GitHub repository, run these commands from this folder. Replace both placeholders first.

```sh
git init
git add .
git commit -m "Publish academic website"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/YOUR-USERNAME.github.io.git
git push -u origin main
```

Then complete steps 3–7 above.

## Before publishing

- Read every line for accuracy, especially 2026 publications and items marked “submitted.” Update statuses as decisions arrive.
- The source CV spells the lead author name in the ACL 2025 entry as “Davis Bartels”; the published paper may display a different spelling. Confirm how you want it shown.
- The source CV is intentionally **not included** because it exposes a phone number and email address. If you add a downloadable CV, export a public version without a phone number, home address, personal metadata, or document comments.
- If you later add contact information, use only an address you are comfortable publishing permanently.
- Consider adding ORCID, Google Scholar, GitHub, and institutional profile links once you have confirmed their URLs.
- Do not add private, embargoed, export-controlled, patient, or employer-confidential material. Anything deployed to normal GitHub Pages should be treated as public.

## Indexing and scraping: what this site does

The site includes several cooperative controls:

- `noindex`, `nofollow`, `noarchive`, `nosnippet`, and `noimageindex` directives in the HTML.
- A `robots.txt` file that blocks several common AI/data crawlers.
- No sitemap, structured-data profile, external fonts, analytics, trackers, or social-preview image.
- No email address or phone number is published.

The wildcard rule in `robots.txt` allows ordinary search crawlers to fetch the page so that they can read its `noindex` directive. Using `Disallow: /` for every bot can be counterproductive: a search engine may know the URL from a link but be unable to crawl the page and see `noindex`.

These controls are requests, not access control. A public URL can still be visited, copied, screenshotted, archived, linked, or scraped by bots that ignore standards.

## If privacy matters more than public reach

Normal GitHub Pages is the wrong place for confidential or genuinely private content. A private repository does not, by itself, make the published Pages site private. Stronger choices are:

1. Keep the site unpublished and share the files directly.
2. Use a host with authentication or password protection.
3. For an organization on GitHub Enterprise Cloud, use a privately published project Pages site with access control.

No public host can both make a page broadly available and guarantee that it will never be scraped.

## Custom domain (optional)

GitHub Pages supports custom domains. Verify the domain in your GitHub account first, then add it in **Settings → Pages** and follow GitHub's DNS instructions. Keep the verification TXT record, enable HTTPS, and remove stale DNS records if you ever disable the site to reduce domain-takeover risk.

## Updating the site

- Edit content in `index.html`.
- Edit appearance in `styles.css`.
- Test on a narrow phone-sized window and a desktop window.
- Commit and push. GitHub Pages typically republishes within several minutes.

## Accessibility and maintenance notes

The site uses semantic headings, a skip link, visible keyboard focus, responsive layouts, reduced-motion support, and print styles. Check new colors for contrast and give any future images useful `alt` text. Review dates, publication status, links, and current affiliations at least twice a year.

## Official references

- [GitHub Pages quickstart](https://docs.github.com/en/pages/quickstart)
- [Creating a GitHub Pages site](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site)
- [Securing a GitHub Pages site with HTTPS](https://docs.github.com/en/pages/getting-started-with-github-pages/securing-your-github-pages-site-with-https)
- [Google: robots meta tags and `X-Robots-Tag`](https://developers.google.com/search/docs/crawling-indexing/robots-meta-tag)
- [Google: introduction to `robots.txt`](https://developers.google.com/search/docs/crawling-indexing/robots/intro)
