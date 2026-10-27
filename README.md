# Niharika's website

A single-page academic portfolio. No build step: it is plain HTML, CSS and JavaScript.

## Files

- `index.html` is the whole site.
- `cv.pdf` is her CV. Add it to this folder (the Download CV buttons point to it). Use a public version without referees' phone numbers. The name must be lowercase: GitHub Pages treats `CV.pdf` and `cv.pdf` as different files.
- `photos/` holds `headshot.jpg` (a square crop shown in the seed head) and the photos in About, Research and Talks. Resize new photos to about 1200px on the long side (under ~300 KB) before adding them. `photos/originals/` keeps the full-size files and is not uploaded.
- `CNAME` is created later, when the domain is ready (see "Custom domain").

## Edit the content

1. Open `index.html` in any text editor and search for `[` to find every placeholder.
2. Publications, talks, news and blog posts are in the `DATA` block near the bottom. Add an item by copying an existing one. Newest first.
3. Wrap her name in `<span class="me">...</span>` inside a publication's authors to highlight it.
4. To show a LinkedIn post: open the post on LinkedIn, choose **Embed this post**, and paste the iframe's `src` address into that news item's `embed:` field.
5. Profile links (Google Scholar, LinkedIn and so on) are in `links:`. A link with an empty `url` stays hidden until you paste the address in. Same for a publication's `doi:`.

Preview locally by double-clicking `index.html`.

## Publish on GitHub Pages

1. Create a free GitHub account for her (or use yours) and a new **public** repository. Name it `niharikavullaganti.github.io` if you want the free address `https://<username>.github.io`, or any name if you will use the custom domain.
2. Upload `index.html` and `cv.pdf` (Add file, then Upload files).
3. In the repository, open **Settings, Pages**. Under "Build and deployment" choose **Deploy from a branch**, branch **main**, folder **/ (root)**, and save.
4. After a minute the site is live at the address shown on that page.

## Custom domain (later)

1. Register `niharikavullaganti.com` at Cloudflare or Porkbun.
2. In **Settings, Pages**, type the domain under "Custom domain" and save. GitHub adds a `CNAME` file for you.
3. At the registrar, add these DNS records (turn the Cloudflare proxy off, "DNS only", for these):
   - Four `A` records for `@` pointing to `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - One `CNAME` record for `www` pointing to `<username>.github.io`
4. Back in **Settings, Pages**, tick **Enforce HTTPS** once it becomes available (it can take up to an hour).

Check GitHub's current Pages documentation if the IP addresses above have changed.

## Notes

- A public repository means the source is visible to everyone. Keep drafts and unpublished data out of it.
- Before posting PDFs of papers, check each publisher's policy. Linking to the DOI is always safe.
