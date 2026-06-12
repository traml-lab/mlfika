# Web pages for the 'ML Fika' Machine Learning Seminar at KTH

This web page uses Jekyll through GitHub Pages, which renders static HTML pages. The
layout auto-supports various screen sizes through Bootstrap.

To install Jekyll locally, follow: [https://jekyllrb.com/docs/installation/](https://jekyllrb.com/docs/installation/).

## Maintaining / Updating

All content is decoupled from the HTML/layout:

- **Series info, organisers, colours, mailing-list link** — edit `_config.yml`.
- **Talks** — add one entry per talk in `_data/talks.yml`. Only `date` and `title`
  are required. If an entry has an `abstract` and/or `biography`, the listing shows
  an "Abstract & bio" toggle that expands those details. Speaker photos are not used.

Talks automatically move from *Upcoming* to *Past* one hour after their scheduled
time, so keep the `date` field parseable (e.g. `September 04, 2026 at 3 pm CEST`).

## Previewing / Running locally

Install Jekyll first, then from the `gh-pages` branch run:

    jekyll serve --baseurl ""

The `--baseurl ""` option overrides the GitHub-specific path so the preview is
available (typically) at http://127.0.0.1:4000/

## Deploying

When deploying to GitHub Pages as a project site (e.g. `https://<org>.github.io/ml-fika`),
set `baseurl: "/ml-fika"` in `_config.yml` so assets resolve correctly.
