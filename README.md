# The Dispatch — deployment guide

This folder is your whole website: `index.html`, `about.html`, `privacy-policy.html`,
`posts.json` (your articles), and `ads.txt` (for later). No coding required to run it.

## 1. Put it online for free — GitHub Pages

1. Go to github.com and create a free account if you don't have one.
2. Click the **+** in the top right → **New repository**. Name it anything,
   e.g. `the-dispatch`. Set it to **Public**. Create it.
3. On the new repo's page, click **"uploading an existing file"** (or drag files in).
4. Upload all the files from this folder: `index.html`, `about.html`,
   `privacy-policy.html`, `posts.json`, `ads.txt`. Commit.
5. Go to the repo's **Settings** tab → **Pages** (left sidebar).
6. Under "Build and deployment," set **Source** to "Deploy from a branch,"
   branch `main`, folder `/ (root)`. Save.
7. Wait a minute, then refresh. GitHub will show your live URL, something like:
   `https://yourusername.github.io/the-dispatch/`

That URL is now public — anyone can visit it.

## 2. Publishing new dispatches

Your articles live in `posts.json`. There are two ways to update it:

**Easy way:** Open your live site, click "File a dispatch," fill it in, and click
"Add & download posts.json." That downloads the updated file to your computer.
Go to your GitHub repo, open `posts.json`, click the pencil (edit) icon, delete
everything, paste in the new file's contents, and commit. Your site updates
within a minute or two.

**Direct way:** Open `posts.json` on GitHub and edit the list by hand — it's
plain JSON, so you can copy an existing entry and change the text.

## 3. Optional: a custom domain

`yourusername.github.io/the-dispatch` works fine to start, and AdSense doesn't
strictly require a custom domain. If you'd rather have something like
`thedispatch.com`, buy a domain (Namecheap, Google Domains successor Squarespace
Domains, etc. — typically $10–15/year, this part isn't free) and point it at
GitHub Pages using their custom domain settings under repo Settings → Pages.

## 4. Applying for Google AdSense

1. Fill out `about.html` and `privacy-policy.html` with real details first —
   don't leave the placeholder text in.
2. Publish several real dispatches (not just the sample post) — Google reviews
   for genuine, original content, not a mostly-empty site.
3. Go to adsense.google.com and sign up with your site's URL.
4. Google gives you a verification snippet to paste into `index.html`'s
   `<head>` (there's a comment marking where it goes). Add it, commit, and
   request review.
5. Review typically takes anywhere from a few days to a few weeks. If rejected,
   the message they send usually says why (commonly: not enough content,
   or navigation/policy pages missing) — fix that and reapply.
6. Once approved, replace `ads.txt`'s placeholder line with the real one
   Google gives you, and add your ad units into the pages.

## Notes

- This site has no backend/database — it's just files. That's what makes it
  free to host, but it also means only you (whoever has repo access) can
  publish; visitors can only read.
- Keep `posts.json` valid JSON — a stray comma will break the page. If that
  happens, GitHub's file history lets you revert to the last working version.
