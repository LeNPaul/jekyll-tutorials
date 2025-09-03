---
permalink: /working-with-content
title: "Configuration Basics"
---

## Content Creation and Management

Content in Jekyll is written in Markdown and controlled with YAML front matter, which adds metadata to each file.

### Using YAML Front Matter

Every post or page starts with a front matter block like:

```yaml
---
title: "My First Post"
date: 2025-09-02
layout: post
categories: tutorials
tags: jekyll basics
---
```

Common keys include:

- `title` – The headline of your content

- `date` – The publishing date

- `layout` – Which template to use (e.g., default, post)

- `permalink` – Customize the URL

### Writing Posts in Markdown

Posts are stored in the `_posts/` folder and must be named with the format:

```bash
YEAR-MONTH-DAY-title.md
```

Jekyll converts Markdown into HTML automatically.

### Pages vs. Posts vs. Drafts

- Posts – Time-based content (e.g., blog entries)

- Pages – Standalone content like "About" or "Contact"

- Drafts – Stored in `_drafts/` and not published until explicitly built

- Future posts – Posts with future dates can be hidden until their time comes, unless you build with `--future`

### Organizing with Categories and Tags

- Categories – Define broad groups for your posts

- Tags – Provide specific labels for filtering