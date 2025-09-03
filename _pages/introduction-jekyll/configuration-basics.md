---
permalink: /configuration-basics
title: "Configuration Basics"
---

The `_config.yml` file is the heart of your Jekyll project. It defines site-wide settings and metadata that Jekyll uses during the build process.

## Editing `_config.yml`

Some common fields include:

- `title` – The name of your site (appears in browser tabs and headers)

- `author` – The name or organization running the site

- `description` – A short description, useful for SEO and feeds

- `baseurl` – The subpath for your site (e.g., `/blog`). Leave it empty if hosted at the root

- `url` – The main domain (e.g., https://example.com)

## Global Variables and Metadata

Variables in _config.yml are accessible throughout your site using Liquid syntax. For example:

```liquid
{% raw %}{{ site.title }}
{{ site.author }}{% endraw %}
```

This helps you reuse data without hardcoding values.