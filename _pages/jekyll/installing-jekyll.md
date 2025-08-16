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

1. Generate a starter Jekyll site
2. Configuring your site (i.e. site name, author, etc.)
3. Adding blog posts
4. Creating and modifying pages
5. Modifying page layouts

## Generate Starter Site

Ensure that Jekyll and Bundler are both installed:

_gem install jekyll bundler_  

Create a new Jekyll site:

_jekyll new myblog_

A new directory will be created with your Jekyll files. Navigate into that directory:

_cd myblog_

Build the site and serve it on your local server:

_bundle exec jekyll serve_

## Explanation

- Do a walk through of the site that was just generated
    - What are the files that get generated when you run jekyll new
    - How those files are used to then build the site under _site
    - What doe it mean to build a Jekyll site
    - What does jekyll serve do? What's the difference between that and deploying an actual website
    - Walk through each directory that is created and the files that are there
- Change the site name and author
- Adding a new blog post
- Changing a blog post layout
- Difference between post and page, and adding a new page

Deploy Jekyll

Deploy to GitHub Pages

Custom domains