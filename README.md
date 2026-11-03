# Team ERSA — SDR Lab website

Static site (hand-written HTML/CSS, no generator) for the Software Defined Radio Lab,
Sharif University of Technology, Fall 2026. Hosted on GitHub Pages.

Members: Amir Mahdi Miraliyari, Mobin Jelodar.

## Layout

```
index.html              Home page: team and the experiments table
assets/style.css        Shared stylesheet (light and dark)
labs/lab00/index.html   Lab 00 setup summary
labs/lab01/index.html   Lab 01 page (pre/post-session sections, math, peer-review comments)
labs/lab01/files/       Files published for Lab 01 (.grc, .py, .pdf, .tex, ...)
.nojekyll               Serve files as-is (no Jekyll processing)
```

## One-time setup

1. The site belongs to the GitHub organization `ersa-sdr`.
2. Inside the organization, create a public repository named exactly `ersa-sdr.github.io`.
3. Upload all files and folders of this site to the repository root.
4. Settings → Pages → Source: *Deploy from a branch*, Branch: `main`, folder `/ (root)`.
5. After 1–2 minutes the site is live at `https://ersa-sdr.github.io/`.
6. Register this address in the course form (deadline: end of week 2).

## Peer-review comments (giscus)

1. Repository → Settings → General → Features → enable **Discussions**.
2. Install the giscus app on the repository: https://github.com/apps/giscus
3. Open https://giscus.app, enter `ersa-sdr/ersa-sdr.github.io`,
   choose mapping *Discussion title contains page pathname* and category *Announcements*.
4. Copy `data-repo-id` and `data-category-id` from the generated snippet into
   `labs/lab01/index.html` (replace `REPO_ID` and `CATEGORY_ID`). Do the same on every new lab page.

## Publishing rule (course regulations, section 5-2)

A report is pushed to this repository **only at the moment of its deadline**, never earlier.
Until then keep the files locally (or in a separate private repository).
After pushing, record the submission time in the course form.

Checklist at each deadline:

1. Copy the files into `labs/labNN/files/`.
2. In `labs/labNN/index.html`, replace the "Published at the deadline" notice with the file list
   (it is already written inside an HTML comment, just uncomment it).
3. Update the status pill of that lab in `index.html`
   (`pill ok` = done, `pill wait` = due, `pill none` = not started).
4. Commit and push, then record the time in the course form.

## Adding a new lab

Copy `labs/lab01/` to `labs/labNN/`, change the title, dates and file list,
paste the giscus IDs, and add a row to the experiments table in `index.html`.

## AI use

The initial HTML/CSS template of this site was drafted with an AI assistant.
