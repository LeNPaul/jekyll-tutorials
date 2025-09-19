---
permalink: /content-creation-management-jekyll
title: "Content Creation and Management in Jekyll"
---

Once you’ve installed Jekyll, created your first site, the next step is learning how to add and manage your content. Jekyll is designed around a simple but powerful model: you write your content in plain text (usually Markdown), add metadata at the top (called front matter), and Jekyll generates the full HTML pages for you.

## YAML Front Matter Explained

Every post and page in Jekyll starts with a YAML front matter block, written between triple dashes (`---`). This block tells Jekyll how to process the file.

```yaml
---
title: "My First Blog Post"
layout: post
date: 2025-09-13
categories: [blog, personal]
tags: [jekyll, tutorial, learning]
---
```

Common keys include:

- `title` – The human-readable title of the post or page.

- `layout` - Which layout template file from `_layouts/` to use (e.g., post, page).

- `date` – The publication date for posts (used in sorting).

- `categories` - Higher-level grouping of content (e.g., blog, portfolio).

- `tags` - Specific labels for organizing content (e.g., jekyll, markdown).

- `permalink` – Override the default URL path for this page/post.

## Writing Content in Markdown

Jekyll supports multiple markup formats, but Markdown is the most common. Markdown is a lightweight syntax for formatting text.

Example:

```markdown
# My First Blog Post

Welcome to my site! This is **bold text**, this is *italic text*, and here’s a [link](https://jekyllrb.com).

- Item 1
- Item 2
- Item 3
```

When you run `jekyll serve`, Jekyll converts this into valid HTML.

## Posts vs. Pages

Jekyll distinguishes between posts and pages:

**Posts**

- Stored in the `_posts/` directory.

- Require a filename format: `YEAR-MONTH-DAY-title.md` (e.g., `2025-09-13-hello-world.md`).

- Usually used for time-based content such as blog entries, news, or chronological content.

- Organized by date and optionally categories/tags.

**Pages**

- Stored in the project root or subdirectories (e.g., about.md).

- No strict naming convention.

- Used for static, standalone content like About, Contact, or Services pages.

- Do not show up in chronological lists unless you configure them to.

## Posts

### Adding Blog Posts

Create a new file in `_posts/` with the correct naming format:

```bash
_posts/2025-09-13-my-first-post.md
```

Add YAML front matter and content:

```yaml
---
title: "My First Blog Post"
layout: post
date: 2025-09-13
categories: [blog, personal]
tags: [jekyll, tutorial, learning]
---
```

Jekyll will automatically regenerate your site with your new post. Run `bundle exec jekyll serve` to preview it locally if your Jekyll site is not already running.

### Drafts and Scheduling Future Posts

Drafts go into a special `_drafts/` folder and don’t need a date in the filename. Example: `_drafts/my-draft-post.md`. Drafts are not published until explicitly built with the `--drafts` flag or moved into `_posts/`. To preview drafts locally: `bundle exec jekyll serve --drafts`.

Jekyll also allows scheduling future posts. If a post has a date later than today, it won’t appear until that date unless you use: `bundle exec jekyll serve --future`.

## Pages

### Modifying Existing Pages

When you generate a new Jekyll site with `jekyll new mysite`, it comes with some starter pages like `about.markdown` and `index.md`. You can:

- Open these files.

- Edit the front matter and content.

- Save changes and rerun the local server.

### Adding New Pages and Updating Navigation

Create a new file in the project root (e.g., contact.md) and add front matter:

```yaml
---
title: "Contact"
layout: page
permalink: /contact/
---
```

The default Jekyll theme, [Minima](https://jekyll.github.io/minima/), will automatically add any pages that you add to the root directory to the site header.

### Organizing Content with Categories and Tags

Jekyll makes it easy to group content using categories and tags:

**Categories:** Broad groupings (like folders). Example: categories: `[blog, travel]`.

**Tags:** Specific labels for filtering. Example: tags: `[jekyll, tutorial, markdown]`.