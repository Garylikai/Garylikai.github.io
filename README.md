# Kai Li's Personal Website

[![Check website](https://github.com/Garylikai/Garylikai.github.io/actions/workflows/check-site.yml/badge.svg)](https://github.com/Garylikai/Garylikai.github.io/actions/workflows/check-site.yml)

Source code and content for [garylikai.github.io](https://garylikai.github.io), the personal academic website of Kai Li.

The site presents my research, publications, teaching and mentoring, academic history, reading notes, and selected personal material. It also provides current PDF copies of my curriculum vitae and industry resume.

## Technology

- [Jekyll](https://jekyllrb.com/)
- [Minimal Mistakes](https://mmistakes.github.io/minimal-mistakes/) 4.28.1, loaded as a remote theme
- [GitHub Pages](https://pages.github.com/) for hosting and deployment
- [Lunr](https://lunrjs.com/) for on-site search
- [MathJax](https://www.mathjax.org/) on pages that contain mathematical notation

## Site structure

- `index.md` — homepage
- `_pages/` — About, Research, Teaching & Mentoring, Reading & Resources, personal notes, and academic-record pages
- `_pages/grad/` — graduate-course and independent-study records
- `_pages/undergrad/` — undergraduate-course and academic-credit records
- `_data/navigation.yml` — primary navigation
- `_data/ui-text.yml` — theme interface text
- `_config.yml` — site metadata, remote-theme settings, search, analytics, and author information
- `_includes/head/custom.html` — page-specific mathematical typesetting support
- `assets/css/main.scss` — site-specific visual adjustments layered over Minimal Mistakes
- `images/` — optimized website images
- `cv.pdf` and `resume.pdf` — downloadable career documents
- `.github/workflows/check-site.yml` — automated build and internal-link checks

## Local preview

Ruby and Bundler are required for a local build.

```bash
bundle install
bundle exec jekyll serve
```

The local site is then available at `http://localhost:4000`. Restart the Jekyll server after changing `_config.yml`.

## Validation and deployment

Changes pushed to the `master` branch trigger two GitHub workflows:

1. GitHub Pages builds and deploys the website.
2. The repository's `Check website` workflow builds the site and uses HTMLProofer to validate generated internal links.

## Routine maintenance

- Replace `cv.pdf` and `resume.pdf` without changing their filenames so existing links remain valid.
- Give every Markdown page a title, permalink, description, layout, and `author_profile` setting in its YAML front matter.
- Use `math: true` only on pages that require mathematical typesetting.
- Keep photographs in web-friendly formats and provide descriptive alternative text.
- Review the live site and the automated checks after significant content or dependency changes.

## Attribution and rights

Minimal Mistakes is created by Michael Rose and distributed under the MIT License. See [`LICENSE`](LICENSE) for the retained theme license and attribution.

Unless otherwise stated, the website's original text, photographs, curriculum vitae, resume, and other personal materials are copyright Kai Li and are not licensed for reuse under the theme's MIT License.
