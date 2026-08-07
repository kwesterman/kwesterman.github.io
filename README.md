# kwesterman.github.io

This site now redirects to the **Westerman Lab** site:
<https://westerman-lab.github.io> (source:
[westerman-lab/westerman-lab.github.io](https://github.com/westerman-lab/westerman-lab.github.io)).

## What is here

| File | Purpose |
| --- | --- |
| `index.html` | Redirects the root URL to the lab site |
| `404.html` | Served for any other path; carries the path over, so `/research/` lands on `/research/` at the lab site |
| `files/` | CV PDFs, kept so existing direct links to them keep working |
| `.nojekyll` | Serves these files as-is instead of running them through Jekyll |

## History

Everything before this point was a full Jekyll site built on the
[AcademicPages](https://github.com/academicpages/academicpages.github.io) theme.
Its content was folded into the lab site. Nothing was lost — the last commit
holding the old site is tagged `personal-site-final`, so it can be restored
with:

```bash
git checkout personal-site-final -- .
```

## Note on redirect type

GitHub Pages cannot issue real HTTP 301s without a custom domain fronted by
another service, so these are client-side redirects (`meta refresh` plus
`location.replace`). Browsers follow them immediately. Search engines treat them
as weaker signals than a 301, which is why both pages carry a `canonical` link
to the lab site and `noindex, follow`.
