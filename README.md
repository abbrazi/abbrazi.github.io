# abbrazi.github.io

A minimal personal website built with Jekyll and hosted on GitHub Pages.

## Structure

| File | Purpose |
| --- | --- |
| `index.md` | About page and homepage (`/`) |
| `blog/index.html` | Automatically lists blog posts (`/blog/`) |
| `code.md` | Projects (`/code/`) |
| `papers.md` | Publications (`/papers/`) |
| `_posts/` | Blog posts in Markdown |
| `_layouts/` | Shared page and post templates |
| `assets/css/style.css` | Shared styles |
| `_config.yml` | Site title, description, navigation, and URLs |

## Edit content

Edit the Markdown pages directly. Set your name and description in `_config.yml`,
then replace the introductory text in `index.md`.

Add a blog post as `_posts/YYYY-MM-DD-post-title.md`:

```markdown
---
title: "My first post"
---

An opening paragraph that also serves as the blog listing excerpt.

More content goes here.
```

Replace `YYYY-MM-DD` with the publication date. Future-dated posts stay hidden
until a build on or after that date; this starter does not schedule builds.
The post layout and active Blog navigation are applied automatically.

Add project links to `code.md` and publication entries to `papers.md`.
PDFs and images can go in `assets/`; link to them with
`[Paper]({{ '/assets/paper.pdf' | relative_url }})`.

## Preview locally

With a current Ruby and Bundler installed:

```sh
bundle install
bundle exec jekyll serve
```

Open <http://localhost:4000>. Restart the server after changing `_config.yml`.
To generate the site without a server, run `bundle exec jekyll build`.

## Publish

This starter works with GitHub Pages' built-in Jekyll build:

1. In the repository, open **Settings → Pages**.
2. Select **Deploy from a branch**, then **main** and **/ (root)**.
3. Commit and push the source files to `main`.

GitHub builds and publishes the site at <https://abbrazi.github.io>.
The generated `_site/` directory is ignored and should not be committed.
