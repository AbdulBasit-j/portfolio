# Getting abdulbasit-j.github.io/portfolio indexed on Google

This needs your Google login, so these are the exact clicks to do it yourself — takes about 10 minutes, plus a few days of waiting for Google to actually crawl it.

## 1. Deploy the site first
Search Console can't verify a site that isn't live. Follow `README.md` to get
`https://abdulbasit-j.github.io/portfolio/` up and running before continuing.

## 2. Add the property in Search Console
1. Go to [search.google.com/search-console](https://search.google.com/search-console).
2. Click **Add property**.
3. Choose the **URL prefix** option (not "Domain") — GitHub Pages subpaths only work with URL-prefix verification, since you don't own the `github.io` domain itself for DNS verification.
4. Enter exactly: `https://abdulbasit-j.github.io/portfolio/`

## 3. Verify ownership (HTML tag method — easiest with GitHub Pages)
1. Search Console will show several verification options. Pick **HTML tag**.
2. It gives you a line like:
   `<meta name="google-site-verification" content="abc123XYZ..." />`
3. Open `index.html`, find this line near the top of `<head>`:
   ```html
   <meta name="google-site-verification" content="REPLACE_WITH_YOUR_VERIFICATION_CODE">
   ```
4. Replace `REPLACE_WITH_YOUR_VERIFICATION_CODE` with the `content` value Google gave you.
5. Commit and push the change so it's live on GitHub Pages.
6. Back in Search Console, click **Verify**.

## 4. Submit your sitemap
1. In Search Console, open **Sitemaps** in the left sidebar.
2. Enter `sitemap.xml` in the field (it'll resolve to `https://abdulbasit-j.github.io/portfolio/sitemap.xml`).
3. Click **Submit**.

## 5. Request indexing directly (speeds things up)
1. Use the **URL Inspection** tool at the top of Search Console.
2. Paste in `https://abdulbasit-j.github.io/portfolio/`.
3. Click **Request Indexing**. Google will crawl it, usually within a few days.

## 6. What actually drives traffic from here
Indexing just means Google *can* show your site — it won't rank you for anything on its own. To get real traffic:
- **Link to it** from places people already see: your GitHub profile README, LinkedIn "Featured" section, and your resume.
- **Backlinks matter more than metadata.** A link from your GitHub profile or a dev.to/Hashnode post about one of these projects is worth far more than any SEO tag.
- **Give Google something to rank you for.** A generic "portfolio" page rarely ranks for anything competitive — but "Spring Boot RBAC example" or "Java expense splitter project" (topics you've actually built) can pick up long-tail search traffic if you ever write about them.
- Check back in Search Console's **Performance** tab after a couple of weeks — it'll show what queries (if any) are surfacing your site, which tells you what to write more of.

## Common snags
- **"Verification failed"**: usually means GitHub Pages hasn't finished redeploying. Wait 2–3 minutes after pushing and retry.
- **Sitemap shows "Couldn't fetch"**: double check `sitemap.xml` is at the repo root and Pages is serving from `/ (root)`, not `/docs`.
- **Property type confusion**: if you ever buy a custom domain, switch to a **Domain** property instead — it covers all subdomains and is the better long-term choice for SEO.
