---
permalink: /jekyll-configuration-basics
title: "Jekyll Configuration Basics"
---

Every Jekyll site has a central YAML configuration file (i.e. `_config.yml`) that controls how the site is built and displayed. This will be your first steps in customizing your project.

## What is YAML

Jekyll relies heavily on YAML (short for YAML Ain’t Markup Language), a human-friendly data format that uses indentation and key-value pairs. YAML is commonly used in configuration files because it is both easy to read and easy to write.

Here’s a simple example of the `_config.yml` YAML file:

```yaml
title: My Awesome Blog
author: Jane Doe
description: "A blog about web development, design, and productivity."
baseurl: "/myblog"
url: "https://janedoe.github.io"
```

Jekyll uses YAML in two main places:

1. `_config.yml` – the main configuration file for your site.

2. Front matter – the block of YAML placed at the top of each page or post inside `---` markers. This defines metadata like the layout, title, or publishing date.

## Editing `_config.yml`

When you run `jekyll new mysite`, Jekyll generates a starter project that includes a file called `_config.yml` at the root of your site. This file is the heart of your Jekyll project. It defines site-wide settings and metadata that Jekyll uses to build your site.

Some common fields include:

- `title` - The title is the name of your site. It often appears in the `<title>` tag of your HTML pages and may also be displayed in headers or navigation menus depending on your theme.

- `author` – The author field identifie the name or organization who owns or writes the site. This value can be displayed in post footers or bios.

- `description` – The description is a short tagline or summary for your site. It is often used in meta tags for SEO and sometimes displayed in headers or footers.

- `baseurl` – Used when your site is hosted in a subpath (e.g., `example.com/blog`). If your site is hosted at the root domain, you can leave it blank (`""`).

- `url` – This should be set to the root URL of your site. Jekyll uses it to generate full, absolute links (e.g., https://example.com).

## Global Variables and Metadata

Any key-value pair you add to `_config.yml` becomes a global variable that you can use throughout your site. For example:

```yaml
twitter: "@janedoe"
email: "jane@example.com"
```

These can then be accessed in your templates or Markdown files using Liquid syntax

```html
<p>Follow me on Twitter: {% raw %}{{ site.twitter }}{% endraw %}</p>
<p>Contact me at: {% raw %}{{ site.email }}{% endraw %}</p>
```

Global metadata like this helps keep your content DRY (Don’t Repeat Yourself). Instead of hardcoding your email address on every page, you define it once in `_config.yml` and reference it wherever needed. If your information changes, you only need to update it in one place.