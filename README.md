# Aryaman Jal — academic website

A small Hugo site for https://aryamanjal.github.io/, using the MIT-licensed
[Hugo Bear Blog](https://github.com/janraasch/hugo-bearblog) theme with local
academic styling. No JavaScript, web fonts, or Node dependencies are required.

## Preview locally

Install [Hugo](https://gohugo.io/installation/) (the workflow uses **0.147.9**), then:

```sh
hugo server --disableFastRender
```

Open http://localhost:1313/. To build the production site:

```sh
hugo --gc --minify --panicOnWarning
```

The generated `public/` directory is ignored by Git.

## Edit content

- `content/_index.md`: biography, research interests, publications, and contact.
- `content/contact.md`: academic email and affiliation.
- `content/teaching.md`: courses and teaching roles.
- `content/activities.md`: collaborative contributions, organization, and outreach.
- `content/cv.md` and `content/research.md`: draft pages, excluded from production.
- `static/images/portrait.jpg`: original uncropped portrait, displayed beside your name; configured with `params.portrait` in `hugo.toml`.
- Papers appear newest first by their initial arXiv posting date.
- `hugo.toml`: site name, description, base URL, and navigation.
- `static/css/academic.css`: typography, colors, spacing, and mobile layout.

The initial text explicitly marks missing information. Replace it with your
details before sharing the site as your completed academic profile.

## Publish on GitHub Pages

In this repository's **Settings → Pages → Build and deployment**, select
**GitHub Actions** as the source. Commit and push these files to `main`.
The included workflow builds Hugo and deploys `public/` to GitHub Pages.
Pull requests build without deploying. No custom domain is needed.

The website address is `https://aryamanjal.github.io/` (there is no `@` in it).

## Theme provenance

The upstream theme is vendored in `themes/hugo-bearblog/` so a fresh clone works
without Git submodules or a theme download during builds. It is pinned to
upstream commit `d6dcedcc75485062723e9f5e8f5d142518b6edef`.
Its original MIT license is retained there. Site-specific overrides are in
`layouts/` and `static/`; the upstream theme files are unchanged.
