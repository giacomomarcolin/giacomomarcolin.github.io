# giacomomarcolin.github.io

A lightweight custom Jekyll site for GitHub Pages. It intentionally uses no
theme and keeps the site content in simple Markdown, YAML, and HTML templates.

## Run locally

Ruby 2.7 or newer and Bundler are required.

```powershell
bundle install
bundle exec jekyll serve --livereload
```

Open <http://localhost:4000>.

To perform the same production build used for deployment:

```powershell
$env:JEKYLL_ENV = "production"
bundle exec jekyll build
```

Generated files are written to `_site/` and are not committed.

## Deploy

The workflow in `.github/workflows/pages.yml` builds and deploys the site when
changes are pushed to `main`. In the repository settings, set **Pages → Build
and deployment → Source** to **GitHub Actions** once before the first deploy.
