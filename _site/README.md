# Communication Theory Primer Website

This repository now contains a Jekyll website configured for GitHub Pages.

## What is included

- Jekyll project scaffold with shared layout and navigation
- Home page plus six required subpages in `/theory/`
- Accessible page structure (semantic landmarks, skip link, ARIA labels)
- Professional blue/green color palette with editable CSS variables
- GitHub Actions workflow at `/home/runner/work/Primer/Primer/.github/workflows/jekyll-build.yml`
- Image folder for your media at `/home/runner/work/Primer/Primer/assets/images/`

## Site structure

```text
/home/runner/work/Primer/Primer/
├── _config.yml
├── _layouts/default.html
├── assets/
│   ├── css/style.scss
│   └── images/
├── index.md
├── theory/
│   ├── transmission-limits.md
│   ├── meaning-culture.md
│   ├── interpretation-power.md
│   ├── interpretation-intention.md
│   ├── reader-guidance.md
│   └── how-this-site-was-built.md
└── .github/workflows/jekyll-build.yml
```

## Writing and editing content

1. Open any page in `/home/runner/work/Primer/Primer/theory/` or the home page `/home/runner/work/Primer/Primer/index.md`.
2. Keep the front matter block (`---` section) at the top of each file.
3. Replace starter paragraphs with your own argument, examples, and citations.
4. Add sections using Markdown headings (`##`, `###`) under the existing page title.
5. Place image files in `/home/runner/work/Primer/Primer/assets/images/` and reference them with:

   ```md
   ![Descriptive alt text]({{ '/assets/images/your-image-file.jpg' | relative_url }})
   ```

6. Use descriptive alt text for all images.

## Customizing visual variables (CSS)

Edit `/home/runner/work/Primer/Primer/assets/css/style.scss` and update values in `:root`:

- `--color-bg`: page background
- `--color-surface`: card/section backgrounds
- `--color-primary`: headings, header, and primary accents
- `--color-secondary`: secondary accent color
- `--color-text`: default text color
- `--color-muted`: secondary text
- `--color-border`: borders
- `--focus-ring`: keyboard focus outline color

After changing colors, verify contrast remains accessible.

## Local preview

From `/home/runner/work/Primer/Primer`:

```bash
bundle install
bundle exec jekyll serve
```

Then open `http://127.0.0.1:4000/Primer/`.

## GitHub Pages build and deploy

The workflow at `/home/runner/work/Primer/Primer/.github/workflows/jekyll-build.yml` runs on every push to `main` and manual dispatch:

- Checks out the repository
- Builds the Jekyll site
- Uploads build artifacts
- Deploys to GitHub Pages

## Notes

- The current content is intentionally boilerplate so you can author your own graded analysis.
- Keep `_config.yml` values aligned with repository location:
  - `url: https://gsamuel2004.github.io`
  - `baseurl: /Primer`
