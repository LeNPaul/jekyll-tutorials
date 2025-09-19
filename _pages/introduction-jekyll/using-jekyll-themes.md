---
permalink: /using-jekyll-themes
title: "Using Jekyll Themes"
---

Jekyll themes let you change your site’s look, layout, and basic UX without rebuilding everything from scratch. They package layouts, includes, and assets into a reusable gem or GitHub repository you can plug into your project with a few lines of config.

## Why Themes Are So Useful and Powerful

- **Separation of concerns:** Content stays in your Markdown files; presentation lives in the theme. Update or swap the theme without touching your posts and pages.

- **Batteries included:** Prebuilt layouts (home, post, page, archives), partials (header, footer, pagination), and styles save hours of boilerplate work.

- **Easy upgrades:** Theme authors ship bug fixes and improvements. You update the gem (or remote theme) and your site benefits.

- **Override when needed:** Jekyll lets you shadow any layout/include/asset by creating a file with the same path in your site—best of both worlds (speed + control).

- **Good defaults for accessibility & SEO:** Most reputable themes ship sensible semantics, meta tags, and mobile-friendly layouts.

## The Default Jekyll Theme

When you run `jekyll new mysite`, Jekyll’s starter site uses the Minima theme by default. You’ll see this in two places:

1. **Gemfile:** includes gem "minima"

2. **`_config.yml`**: contains theme: minima

Minima provides standard blog layouts, a basic home page, post styling, and sensible typography—perfect for learning Jekyll before you customize.

## Using a Different Theme

You have two primary ways to use themes:

1. Gem-based theme (installed through RubyGems)

2. Remote theme (pulled from a GitHub repo at build time)

Choose one approach per project (don’t set both `theme:` and `remote_theme:` at the same time).