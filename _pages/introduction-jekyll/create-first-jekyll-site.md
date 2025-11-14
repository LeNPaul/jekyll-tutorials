---
permalink: /create-first-jekyll-site
title: "Create Your First Jekyll Site"
---

In this module, you’ll set up Jekyll on your machine, create your very first Jekyll site, and explore how Jekyll organizes a project. By the end, you’ll have a working local development environment where you can view your Jekyll site in a browser.

## Setup & Installation

Before you can start creating with Jekyll, you’ll need to install some dependencies and set up your development environment. This section will walk you through installing the necessary tools, setting up Jekyll, and creating your first Jekyll site.

### Setting Up Your Development Environment

Jekyll is built with Ruby, so the first step is ensuring you have Ruby installed on your machine. Along with Ruby, you’ll also need RubyGems (Ruby’s package manager), a compiler (GCC and Make), and Bundler, which manages project dependencies.

Once these are installed, you’ll be able to install and run Jekyll.

#### Installing Ruby & RubyGems

##### macOS

macOS usually comes with Ruby pre-installed, but it might be an outdated version.

You can check your Ruby version with:

```bash
ruby -v
```

If you need the latest Ruby, install Homebrew (a popular package manager for macOS) and run:

```bash
brew install ruby
```

RubyGems (Ruby’s package manager) is included with Ruby, so no extra steps are required. After installation, verify with:

```bash
ruby -v
gem -v
```

##### Linux (Ubuntu/Debian)

Update your package list and install Ruby + dependencies:

```bash
sudo apt update
sudo apt install ruby-full build-essential zlib1g-dev
```

Add Ruby’s bin directory to your shell configuration:

```bash
echo 'export PATH="$HOME/gems/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc
```

Verify installation:

```bash
ruby -v
gem -v
```

##### Windows

The easiest way is to install RubyInstaller for Windows: https://rubyinstaller.org

During installation, check the box to install MSYS2 development tools (needed for compiling).

Once finished, open a new command prompt and verify:

```bash
ruby -v
gem -v
```

#### Installing Jekyll & Bundler

With Ruby installed, you can install Jekyll and Bundler (manages Ruby gem dependencies for your project) via RubyGems gems globally:

```bash
gem install jekyll bundler
```

Run the following to confirm Jekyll is installed (if you see a version number, your installation is successful):

```bash
jekyll -v
bundle -v
```

## First Jekyll Site

Now that Jekyll is installed, let’s create your first site.

### Creating a Simple New Jekyll Site

Run:

```bash
jekyll new mysite
cd mysite
```

This generates a starter project with a predefined structure in the `mysite/` folder.

### Anatomy of a Jekyll Site

When you open the `mysite/` folder, you’ll see something like this:

```bash
mysite/
├── 404.html
├── about.markdown
├── index.markdown
├── _config.yml
├── _posts/
│   └── 2025-09-06-welcome-to-jekyll.markdown
├── _site/            # (created after first build)
├── Gemfile
└── Gemfile.lock      # (created after running bundle install)
```

Here’s what each part does:

- 404.html – A simple error page displayed when someone visits a non-existent URL.

- about.markdown – A sample “About” page written in Markdown.

- index.markdown – The home page of your site.

- _config.yml – The central configuration file. You define your site title, author, URL, theme, plugins, and other global settings here.

- _posts/ – Contains your blog posts. Jekyll names posts with the format YYYY-MM-DD-title.md. A sample “Welcome to Jekyll!” post is included by default.

- _site/ – Generated automatically when you build or serve your site. It contains the final static HTML, CSS, and JS files that are ready to deploy. Do not edit this folder directly.

- Gemfile – Lists the Ruby gems (dependencies) your site needs, including Jekyll itself and the default theme.

- Gemfile.lock – Created when you run bundle install. It locks gem versions to ensure consistency across different environments.

By default, the new site uses the minima theme, which provides layouts, includes, and styling. Those theme files don’t appear in your folder because they live inside the gem (you can override them to customize your site, which we will cover in a different course).

### Running the Local Development Server

Start your Jekyll server with:

```bash
bundle exec jekyll serve
```

This will build your Jekyll site and make it available locally at `http://localhost:4000` in your browser. Any changes you make to any project files (except inside `_site/`) will automatically update your site.

### Understanding `_site/`

When you run `jekyll build` or `jekyll serve`, Jekyll generates a folder called `_site/` which contains the final static HTML, CSS, and JavaScript files that gets published when you deploy your site. You normally don’t edit files in `_site/`, since they're regenerated automatically every time Jekyll builds your site.

At this point, you have Jekyll installed, a new Jekyll site created, and a development Jekyll server running. You’re ready to start customizing your site!