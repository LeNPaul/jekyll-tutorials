---
permalink: /jekyll-basics
title: "Working with Jekyll Basics"
---

This module introduces you to the core structure of a Jekyll site and walks through how to configure, create, and style content. By the end, you’ll be able to set up a basic site, write posts and pages, and customize layouts with themes and templates.

## Configuration Basics

The `_config.yml` file is the heart of your Jekyll project. It defines site-wide settings and metadata that Jekyll uses during the build process.

### Editing `_config.yml`

Some common fields include:

- `title` – The name of your site (appears in browser tabs and headers)

- `author` – The name or organization running the site

- `description` – A short description, useful for SEO and feeds

- `baseurl` – The subpath for your site (e.g., `/blog`). Leave it empty if hosted at the root

- `url` – The main domain (e.g., https://example.com)

### Global Variables and Metadata

Variables in _config.yml are accessible throughout your site using Liquid syntax. For example:

```liquid
{% raw %}{{ site.title }}
{{ site.author }}{% endraw %}
```

This helps you reuse data without hardcoding values.

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

- title – The headline of your content

- date – The publishing date

- layout – Which template to use (e.g., default, post)

- permalink – Customize the URL

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

## Layouts and Includes

Jekyll uses a templating system to keep your design consistent

### Default Layouts

Stored in the _layouts folder, layouts wrap around your content. For example:

- `default.html` – The base wrapper for all pages.

- `post.html` – Specific to blog posts.

By the end of this module, you’ll have a functional Jekyll site with structured content, navigation, layouts, and styling that can easily be extended with themes and custom designs.