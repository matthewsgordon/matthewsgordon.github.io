# matthewsgordon.github.io

My personal website, built with [Jekyll](https://jekyllrb.com/) and hosted on
[GitHub Pages](https://pages.github.com/).

## Sections

The site has a navigation menu with three main sections:

- **Posts** — blog entries and articles (in `_posts/`)
- **Projects** — software projects and publications (in `_projects/`)
- **About** — a static profile page (`about.md`)

## Structure

```
.
├── _config.yml          # Site configuration
├── _data/navigation.yml # Menu navigation items
├── _includes/           # Reusable HTML fragments (header, footer, head)
├── _layouts/            # Page templates (default, home, page, post)
├── _posts/              # Blog posts (YYYY-MM-DD-title.md)
├── _projects/           # Projects & publications collection
├── about.md             # About page
├── posts.md             # Posts listing page
├── projects.md          # Projects listing page
├── index.md             # Homepage
└── Gemfile              # Ruby dependencies
```

## Local development

```bash
bundle install      # first time only
bundle exec jekyll serve --livereload
```

Then open <http://localhost:4000>.

To build the site without serving:

```bash
bundle exec jekyll build
```

The generated site is output to `_site/`.

## Adding content

### New blog post

Create `_posts/YYYY-MM-DD-my-title.md`:

```yaml
---
layout: post
title: My title
date: 2026-08-18
---
Your content here.
```

### New project or publication

Create `_projects/YYYY-MM-DD-name.md` and set the `type` field to either
`project` or `publication`. The listing page uses fields like `title`,
`link`, `authors`, `venue`, `year`, and `description`.
