---
permalink: /getting-started-jekyll
title: "Getting Started with Jekyll"
---

In this module, you’ll set up Jekyll on your machine, create your very first site, and explore how Jekyll organizes a project. By the end, you’ll have a working local development environment where you can view your site in the browser.

## Setup & Installation

Before working with Jekyll, you’ll need to install some dependencies.

### Installing Ruby & RubyGems

Jekyll is built with Ruby, so you must have Ruby installed. Most systems (macOS and Linux) already come with Ruby pre-installed, but it’s recommended to install the latest stable version. RubyGems (Ruby’s package manager) is included with Ruby, so no extra steps are required.

### macOS

Use Homebrew

```bash
brew install ruby
```

### Linux (Ubuntu/Debian)

```bash
sudo apt-get install ruby-full build-essential zlib1g-dev
```

### Windows

Install Ruby via the RubyInstaller

### Installing Jekyll & Bundler

With Ruby ready, install Jekyll (the static site generator) and Bundler (manages Ruby gem dependencies for your project) gems globally:

```bash
gem install jekyll bundler
```

### Verifying Installation

Check if everything is installed correctly:

```bash
jekyll -v
bundle -v
```

If you see version numbers, you’re ready to move on.

## First Jekyll Site

Now let’s create your first Jekyll site and learn how the project is structured.

### Creating a New Jekyll Site

Run:

```bash
jekyll new mysite
cd mysite
```

This will generate a starter site with the necessary files and folders.

### Understanding the Project Structure

Inside the new folder, you’ll see something like this:

`_config.yml` – The main configuration file (site settings, metadata, plugins).

`_layouts/` – Templates that define the overall structure of pages (e.g., default, post).

`_includes/` – Reusable snippets (like headers, footers, navigation menus).

`_posts/` – Blog posts, stored with filenames in the format YYYY-MM-DD-title.md.

`_data/` – YAML, JSON, or CSV files to store structured data for use across the site.

`assets/` – Static files such as images, CSS, and JavaScript.

`index.md` – The home page of your site.

`Gemfile` – Defines Ruby gem dependencies for your project.

### Running the Local Development Server

Start your server with:

```bash
bundle exec jekyll serve
```

By default, your site will be available at http://localhost:4000.

### Understanding `_site`

When you build or serve your project, Jekyll generates a `_site` folder. This is the compiled output—the HTML, CSS, and JS that will be deployed to the web server. You normally don’t edit files in _site, since it’s regenerated automatically every time you build.

Congratulations! You’ve just set up your first Jekyll site and seen it running locally.