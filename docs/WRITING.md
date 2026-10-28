# Writing workflow

This site uses Hugo and Markdown for content. Most publishing is done directly in the repository with a simple `hugo new` workflow.

## Create a draft article

From the project root:

```bash
hugo new content blog/my-first-post.md
```

This creates a Markdown file with front matter. Start the file with a title, summary, and tags:

```yaml
---
title: "My First Post"
date: 2026-10-28
summary: "A short summary of the article."
tags: ["python", "backend"]
draft: true
---
```

Write the article in Markdown below the front matter.

## Preview locally

```bash
hugo server -D
```

Then open the URL printed in the terminal, usually http://localhost:1313/.

## Publish an article

When the draft is ready:

1. Set `draft: false`
2. Optionally add an `updated` date
3. Commit the change
4. Push to GitHub
5. Cloudflare Pages will rebuild automatically if connected to the `main` branch

## Add a project entry

Project entries are kept in `data/projects.yaml` and rendered from the projects page. Each item includes:

- name
- description
- source
- demo (optional)
- technologies

## Update biography and navigation

Main config and site-wide content live in:

- `hugo.toml`
- `data/site.yaml`

These central files are the easiest place to edit the name, site URL, social media links, and navigation.

## Build production output

```bash
hugo --minify
```

This writes the final static site to `public/`.
