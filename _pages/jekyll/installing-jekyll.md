---
permalink: /installing-jekyll
title: "Installing Jekyll"
---

## Setting Up Your Development Environment

To make working with Jekyll smoother, you’ll want a development environment that includes:

### Code Editor/IDE

While you can edit files with any text editor, using a modern IDE makes the process easier. At a minimum, ensure your editor has syntax highlighting for Markdown, HTML, YAML, and Ruby:

1. **VS Code (recommended):** Free, lightweight, and has extensions for Markdown, Git, and Ruby.

2. **Sublime Text:** Fast and simple, with good plugin support.

### Terminal/Command Line

You’ll be using the terminal frequently to install dependencies, run jekyll serve, and deploy your site.

1. **macOS/Linux:** Use the built-in terminal.

2. **Windows:** PowerShell works fine, but Git Bash or Windows Subsystem for Linux (WSL) is often better.

## Requirements

The following is a list of everything needed to install and run Jekyll:

1. **Ruby:** Jekyll is built using the Ruby programming language

2. **RubyGems:** Jekyll itself is a Ruby gem, which is Ruby code that has been packaged into a self-contained project, so you will need the RubyGems package manager to install Jekyll

3. **GCC and Make:** Compilers for compiling Ruby code

4. **Bundler:** Technically optional, Bundler is a Ruby gem that is used to install all of the gems in your Gemfile, a file that contains a list of all of the gems needed to run your Jekyll site—we will cover this in more detail later on

To install all of the requirements, please reference [the Installation page on the official Jekyll site](https://jekyllrb.com/docs/installation/), which already offers comprehensive instruction.