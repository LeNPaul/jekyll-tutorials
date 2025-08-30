---
permalink: /create-simple-jekyll-site
title: "Create a Simple Jekyll Site"
---

Once we have Jekyll installed, we can now create a simple Jekyll site. The goal here is to generate a simple but useful Jekyll site to use as a starter for learning the basics of how to work with Jekyll. We will cover the following topics:

1. Generate Starter Site

2. Configuring Your Site

3. Adding Blog Posts

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

Jekyll will compile the site and serve it at `http://localhost:4000`. With the exception of `_config.yml`, any changes you make to the files will automatically be reflected.

## Configuring Your Site

When you run `jekyll new myblog`, Jekyll scaffolds a starter site for you. Configuring it properly is the first step to making it your own. Before we go into depth with all of the files and directories generated, we will start with basic configuration.

Open `_config.yml` in your editor and try changing these fields:

```yaml
title: <your site title>
email: <your-email@example.com>
description: <your description>
```

Since we made changes to the `_config.yml` file, you will need to restart your Jekyll server for the changes to be applied. You can stop the Jekyll server with `CRTL + C` and run `bundle exec jekyll serve` again.

## Adding Blog Posts

Blog posts go inside the `_posts/` directory. There should already be a sample blog post in the `_posts/` directory with a filename format of:

```bash
YEAR-MONTH-DAY-title.md
```

Example:

```bash
2025-08-30-hello-world.md
```

Open the file in your IDE, and add the configuration, called the front matter, and the top of file:

```yaml
---
layout: post
title: "Hello World"
date: 2025-08-30
---
```

Write some [Markdown](https://www.markdownguide.org/) content below the front matter. Jekyll will automatically update your site and serve it at `http://localhost:4000`.