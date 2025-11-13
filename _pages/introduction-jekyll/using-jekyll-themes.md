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

When you run `jekyll new mysite`, Jekyll’s starter site uses [the Minima theme](https://jekyll.github.io/minima/) by default. You’ll see this in two places:

1. **Gemfile:** includes gem "minima"

2. **`_config.yml`**: contains theme: minima

Minima provides standard blog layouts, a basic home page, post styling, and sensible typography—perfect for learning Jekyll before you customize.

## Using a Different Theme

You have two primary ways to use themes:

1. Gem-based theme (installed through RubyGems)

2. Remote theme (pulled from a GitHub repo at build time)

Choose one approach per project (don’t set both `theme:` and `remote_theme:` at the same time).

### Using a Gem-Based Theme

1. Find and install the theme gem: in your project’s `Gemfile`, add (or replace Minima with) another theme gem, for example:

    ```yaml
    gem "jekyll-theme"
    ```

2. Install with `bundle install`

3. Point Jekyll at the new theme in `_config.yml`:

    ```yaml
    theme: jekyll-theme
    ```

4. Run the site with `bundle exec jekyll serve`

### Using a Remote Theme

1. Add the plugin in your `Gemfile`:

    ```yaml
    gem "jekyll-remote-theme"
    ```

2. Enable and configure in `_config.yml` (remove any `theme:` line to avoid conflicts):

    ```yaml
    plugins:
    - jekyll-remote-theme

    # Replace with the owner/repo of the theme you want:
    remote_theme: owner/theme-repo
    ```

3. Serve locally with `bundle exec jekyll serve`

## Common Customizations

- Override index.md/html or _layouts/home.html to customize the home page.

- Site navigation can be customeized on many themes—check your theme’s docs.

- Social icons & metadata are often configured via `_config.yml` keys (e.g., twitter_username, github_username).

## Troubleshooting Tips

- “Theme could not be found”

    - For gem themes, ensure it’s in your `Gemfile` and run `bundle install`.

    - For remote themes, verify:
    
        ```yaml
        plugins: 
        - jekyll-remote-theme 
        
        # Point to a public owner/repo.
        remote_theme: owner/theme-repo
        ```

- Conflicting settings: use either `theme:` (gem) or `remote_theme:` (GitHub repo), not both.

- Assets not loading: check your `baseurl` and `url` in `_config.yml`, especially when viewing under a subpath (e.g., GitHub Pages project sites).

- Sass not compiling: make sure your Sass file has front matter (`---`on the first two lines) so Jekyll processes it.

- Locked versions on GitHub Pages: if using `github-pages`, your gem versions are pinned—use `remote_theme` to use the latest upstream theme.