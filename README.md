# Portfolio — Abdul Basit

A single-file static site (`index.html`) showcasing 9 full-stack Java/Spring Boot + React/Angular projects. No build step required.

## Deploy to GitHub Pages (matches your target URL: `abdulbasit-j.github.io/portfolio/`)

1. Create a new repo on GitHub named exactly **`portfolio`** (must match, since your URL includes `/portfolio/`).
2. Upload these three files to the **root** of that repo:
   - `index.html`
   - `robots.txt`
   - `sitemap.xml`
3. In the repo, go to **Settings → Pages**.
4. Under **Build and deployment → Source**, choose **Deploy from a branch**.
5. Set **Branch** to `main` and folder to `/ (root)`, then **Save**.
6. Wait 1–2 minutes. Your site goes live at:
   `https://abdulbasit-j.github.io/portfolio/`

### Quick way via terminal (if you have git installed)
```bash
git init
git add index.html robots.txt sitemap.xml
git commit -m "Launch portfolio"
git branch -M main
git remote add origin https://github.com/abdulbasit-j/portfolio.git
git push -u origin main
```
Then turn on Pages as in step 3–5 above.

## Before you publish, update:
- **Email**: already set to `basitjatoi17@gmail.com` — update in `index.html` if this changes.
- **google-site-verification meta tag** in `<head>` of `index.html` — you'll get this exact string in Step 2 of `SEARCH_CONSOLE_GUIDE.md`. Paste it in, replacing `REPLACE_WITH_YOUR_VERIFICATION_CODE`, then redeploy before verifying in Search Console.

## Next steps
See `SEARCH_CONSOLE_GUIDE.md` for getting this site indexed on Google.
