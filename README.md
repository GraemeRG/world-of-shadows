# World of Shadows

A gothic-Victorian Jekyll site for project showcases and writings, built for GitHub Pages.

Live at: https://graemerg.github.io/world-of-shadows/

## Adding a new blog post

Create a file in `_posts/` named `YYYY-MM-DD-your-title.md`:

```markdown
---
title: "Your Title"
date: 2026-07-04
tags: [tag-one, tag-two]
excerpt: "One sentence summary shown in listings."
---

Your content here, in Markdown.
```

## Adding a new project

Create a file in `_projects/` (filename becomes the URL slug, e.g. `_projects/my-game.md`):

```markdown
---
title: "Project Name"
date: 2026-07-04
tagline: "One-line description."
stack: ["Tech", "Stack", "Items"]
links:
  - label: "Source"
    url: "https://github.com/you/repo"
---

Project writeup in Markdown. Use `![alt](/assets/images/foo.png)` for images
(drop image files into `assets/images/`).
```

## Running locally

Requires Ruby + Bundler.

```bash
bundle install
bundle exec jekyll serve
```

Then visit `http://localhost:4000/world-of-shadows/`.

## Publishing

1. Push this repo to GitHub as `world-of-shadows`.
2. In the repo's Settings → Pages, set Source to "Deploy from a branch", branch `main`, folder `/ (root)`.
3. GitHub will build it automatically. It can take a minute or two on first deploy.
4. Site will be live at `https://graemerg.github.io/world-of-shadows/`.

## Adding a custom domain later

1. Add a `CNAME` file to the repo root containing just your domain, e.g. `worldofshadows.com`.
2. At your domain registrar, add either:
   - An `A` record pointing the apex domain to GitHub's IPs (185.199.108.153, .109.153, .110.153, .111.153), or
   - A `CNAME` record if using a subdomain like `www.worldofshadows.com`.
3. In repo Settings → Pages, enter the custom domain and enable "Enforce HTTPS" once DNS propagates.
4. Update `url` in `_config.yml` to the new domain and set `baseurl` to an empty string (since a custom domain typically serves from root).
