---
permalink: /deploying-hosting-jekyll
title: "Deploying and Hosting Jekyll"
---

Once you’ve built your Jekyll site locally, the next step is to publish it on the web. Jekyll generates static HTML files, which means you have a wide range of hosting options—from GitHub Pages (most popular) to dedicated static-hosting platforms like Netlify, Vercel, or Amazon S3.

This module walks you through everything you need to know to build your site for production, host static files, and deploy using GitHub Pages.

## Building the Site for Production

Before deployment, Jekyll needs to convert your Markdown, layouts, and theme files into static HTML. This is called “building” the site, and is done with the following command:

```yaml
bundle exec jekyll build
```

This creates a complete, production-ready version of your website inside the `/_site` directory.

During a build, Jekyll will:

- Read your `_config.yml`

- Process Markdown, Liquid templates, and collections

- Apply your theme and layouts

- Copy over assets (CSS, JS, images)

- Generate final static HTML files

## How to Serve Static Website Files

Once your site is built, the output folder (`_site/`) contains nothing but HTML, CSS, JavaScript, and images—pure static files. There’s no database, no backend, and no server-side logic. That means any static hosting provider can serve it.

When serving static files, a static host will:

- Store your generated files

- Respond to visitor requests for files 

- Send requested files to the browser (e.g., `index.html`)

## Deploying Jekyll to GitHub Pages

Because Jekyll sites are static, you have many hosting choices. GitHub Pages is the simplest and most popular hosting option for Jekyll—especially for beginners:

- Native Jekyll support

- Free hosting

- Automatic builds via GitHub Actions

- Comes with a default domain: username.github.io

GitHub can automatically build your site whenever you push code to your repository.