# STALA 2027 website

Source for **https://stala-workshop.github.io**, the website of STALA 2027, the Workshop on Security Testing and Assurance for LLMs and Agents, co-located with the NDSS Symposium 2027 in Seoul.

The site is a single static page served by GitHub Pages. It has no build step, no framework and no dependencies. Fonts load from Google Fonts.

## Files

| File | Purpose |
|---|---|
| `index.html` | The whole website: content, styles and the small interactive script |
| `404.html` | Page shown for broken links |
| `favicon.svg` | Browser-tab icon |
| `og-image.png` | Preview image (1200×630) shown when the link is shared on Slack, X, LinkedIn or email |
| `robots.txt`, `sitemap.xml` | Help search engines index the site |
| `.nojekyll` | Tells GitHub Pages to serve the files as they are, without Jekyll processing |

## Editing

1. Open `index.html` on GitHub and click the pencil icon (**Edit this file**).
2. Use Ctrl/Cmd + F to find the text you want to change. Each part of the page is a `<section>` with its own id: `about`, `cfp`, `dates`, `program`, `people`, `venue`.
3. Click **Commit changes**. The live site updates within about a minute.

Things that commonly need updating:

- **Submission link.** Search for `Opens soon` and replace that `<span class="tba">…</span>` with a link.
- **Keynote II.** Search for `Speaker to be announced` (program) and `To be announced` (People).
- **Dates.** Each item in the Important dates list has a `data-date="YYYY-MM-DD"` attribute. The Passed / Next / Upcoming labels and the deadline countdown are calculated from these dates (Anywhere on Earth), so change the attribute along with the visible text. The countdown deadline is also set near the end of the script: `aoeEnd('2026-12-11')`.
- **Program committee.** Replace the text in the `pc-note` block with the list of names.
- **After editing dates or content,** update `<lastmod>` in `sitemap.xml`.

## Hosting setup (one-off)

- The repository must be named exactly `stala-workshop.github.io` and belong to the GitHub organisation `stala-workshop`.
- In **Settings → Pages**, set **Source** to **Deploy from a branch**, **Branch** to `main` and the folder to `/ (root)`.
- No `CNAME` file is needed while the site uses the `github.io` address.

## Organisers

Stjepan Picek, Wenkai Xu, Lichao Wu and Alexandra Dmitrienko (Workshop Co-Chairs); Nan Lu (Publicity Chair).
