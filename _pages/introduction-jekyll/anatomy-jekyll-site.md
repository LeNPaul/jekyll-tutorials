---
permalink: /anatomy-jekyll-site
title: "Anatomy of a Jekyll Site"
---

When you run `jekyll new myblog`, Jekyll creates a starter site with a standard set of files and directories:

### _config.yml

The main configuration file. You’ll edit this to change things like your site’s title, author, description, and theme.

### _posts/

Contains your blog posts. Each post is a Markdown file where the name is structured as `YEAR-MONTH-DAY-title.md`.

### _layouts/

Holds templates that define the overall structure of pages. For example, `default.html` wraps around all pages, and `post.html` defines how blog posts look.

### _includes/

Stores reusable snippets (such as a navigation bar or footer) that you can insert into layouts with Liquid tags.

### _site/

This is the output directory. When you run `jekyll build`, Jekyll takes your source files, processes them through layouts, and generates the final static HTML site here. Note: You should not edit files in `_site` directly because they are regenerated each time you build the site.

### index.md

The homepage of your site. By default, this is a Markdown file that uses a layout template.

### Gemfile

Lists Ruby gems (dependencies) your project uses, including Jekyll and plugins.

### _data/

A place for YAML, JSON, or CSV files that provide structured data. These files are accessible in your templates via `site.data`.

### _drafts/

Stores unpublished posts. Drafts won’t appear on your site unless you run Jekyll with the `--drafts` flag or move them into `_posts/`.

### _sass/

Contains Sass partials that get imported into your main stylesheet. This keeps your styles modular and easier to maintain.

### assets/

Holds images, stylesheets, JavaScript, and other static files that your site uses.

### _plugins/

Custom Ruby plugins that extend Jekyll’s functionality, such as generators and filters.
