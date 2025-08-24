---
permalink: /create-simple-jekyll-site
title: "Create a Simple Jekyll Site"
---

Once we have Jekyll installed, we can now create a simple Jekyll site. The goal here is to generate a simple but useful Jekyll site to use as a starter for learning the basics of how to work with Jekyll. We will cover the following topics:

1. Generating a starter Jekyll site

2. Configuring your site (i.e. site name, author, etc.)

3. Adding blog posts

4. Creating and modifying pages

5. Modifying page layouts

## Generate Starter Site

Ensure that Jekyll and Bundler are both installed:

```bash
gem install jekyll bundler
```

Create a new Jekyll site:

```bash
jekyll new myblog
```

A new directory will be created with your Jekyll files. Navigate into that directory:

```bash
cd myblog
```

Build the site and serve it on your local server:

```bash
bundle exec jekyll serve
```

## Configuring Your Site

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