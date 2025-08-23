---
permalink: /installing-jekyll
title: "Installing Jekyll"
---

## Requirements

The following is a list of everything needed to install and run Jekyll:

1. **Ruby:** Jekyll is built using the Ruby programming language
2. **RubyGems:** Jekyll itself is a Ruby gem, which is Ruby code that has been packaged into a self-contained project, so you will need the RubyGems package manager to install Jekyll
3. **GCC and Make:** Compilers for compiling Ruby code
4. **Bundler:** Technically optional, Bundler is a Ruby gem that is used to install all of the gems in your Gemfile, a file that contains a list of all of the gems needed to run your Jekyll site—we will cover this in more detail later on

To install all of the requirements, please reference [the Installation page on the official Jekyll site](https://jekyllrb.com/docs/installation/), which already offers comprehensive instruction.

## Create a Simple Jekyll Site

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

## Exploring the Generated Site

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