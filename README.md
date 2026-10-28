# Md. Nisab Bin Zahid

A minimalist Hugo-based personal website and technical blog inspired by a typography-focused engineering journal.

## Local development

```bash
hugo server -D
```

Then open http://localhost:1313/

## Build for production

```bash
hugo --minify
```

## Create a blog post

```bash
hugo new content blog/my-first-post.md
```

Set `draft: false` when ready to publish.

## Main files

- `hugo.toml` — site configuration
- `data/site.yaml` — name, intro, social links, navigation
- `data/projects.yaml` — project entries
- `content/` — pages and blog posts
- `docs/WRITING.md` — article publishing workflow
- `static/` — static assets
