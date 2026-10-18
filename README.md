# STALA 2027 website

Source for **https://stala-workshop.github.io**, the website of STALA 2027, the Workshop on Security Testing and Assurance for LLMs and Agents, co-located with the NDSS Symposium 2027 in Seoul.

The site is a single static page served by GitHub Pages. It has no build step, no framework and no dependencies; small inline scripts highlight the menu tab of the section in view and provide the light/dark switch. Fonts load from Google Fonts.

## Files

| File | Purpose |
|---|---|
| `index.html` | The whole website: content, styles and the menu-highlight and light/dark scripts |
| `404.html` | Page shown for broken links |
| `favicon.svg` | Browser-tab icon |
| `og-image.png` | Preview image (1200×630) shown when the link is shared on Slack, X, LinkedIn or email |
| `robots.txt`, `sitemap.xml` | Help search engines index the site |
| `.nojekyll` | Tells GitHub Pages to serve the files as they are, without Jekyll processing |

## Editing

1. Open `index.html` on GitHub and click the pencil icon (**Edit this file**), or edit a local clone and push.
2. Use Ctrl/Cmd + F to find the text you want to change. Each part of the page is a `<section>` with its own id: `cfp`, `dates`, `program`, `committee`, `attend`.
3. Commit the change. The live site updates within about a minute.

Things that commonly need updating:

- **Submission link.** Search for `Opens soon` and replace that `<span class="tba">…</span>` with a link.
- **Program committee.** Search for `To be announced` in the `committee` section and replace it with the list of names.
- **Dates.** The paper deadline and workshop date appear twice: in the summary boxes at the top (`class="facts"`) and in the Important Dates list. Change both.
- **Program.** The tentative program is the table in the `program` section.
- **After editing content,** update `<lastmod>` in `sitemap.xml`.

## Hosting setup (one-off)

- The repository must be named exactly `stala-workshop.github.io` and belong to the GitHub organisation `stala-workshop`.
- In **Settings → Pages**, set **Source** to **Deploy from a branch**, **Branch** to `main` and the folder to `/ (root)`.
- No `CNAME` file is needed while the site uses the `github.io` address.

## Organisers

Lichao Wu, Wenkai Xu, Stjepan Picek and Alexandra Dmitrienko (Workshop Co-Chairs); Nan Lu (Publicity Chair).
