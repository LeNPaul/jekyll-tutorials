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

## Common Ways to Host a Jekyll Site

Because Jekyll sites are static, you have many hosting choices. GitHub Pages is the simplest and most popular hosting option for Jekyll—especially for beginners:

- Native Jekyll support

- Free hosting

- Automatic builds via GitHub Actions

- Comes with a default domain: username.github.io

GitHub can automatically build your site whenever you push code to your repository.

## Deploying Jekyll to GitHub Pages

### Installing Git

Before deploying, make sure Git is installed on your system:

- macOS

    - Git usually comes pre-installed. Check with:

        ```bash
        git --version
        ```

    - If not installed, install via Homebrew:

        ```bash
        brew install git
        ```

- Ubuntu/Debian Linux

    ```bash
    sudo apt update
    sudo apt install git
    ```

- Windows

    - Install Git for Windows: https://git-scm.com/download/win

### Setting Up Your GitHub Account and Repository

1. Create a GitHub Account

    - If you don’t already have one: https://github.com/join

2. Create a New Repository for Your Site

    1. Log in to GitHub

    2. Click New Repository

    3. Name it:

        - For a personal site: username.github.io

        - For any other site: any name is fine

    4. Choose Public

    5. Click Create Repository

3. Initialize Git Locally

    - Navigate to your Jekyll project folder:

        ```bash
        git init
        git add .
        git commit -m "Initial Jekyll site"
        ```

4. Connect Local Folder to GitHub

    - GitHub provides a remote URL—copy it and run:

        ```bash
        git remote add origin https://github.com/<username>/<repo>.git
        git push -u origin main
        ```

### Setting Up Your Jekyll Site to Run on GitHub Pages

There are two ways to host with GitHub Pages:

#### Option A: GitHub Builds Jekyll for You (Recommended for Beginners)

GitHub supports a limited set of plugins but automatically builds Jekyll.

Steps:

1. Go to your repository settings

2. Click Pages

3. Under Source, choose:

    - GitHub Actions (new recommended way)

4. GitHub will auto-create a workflow to build your site

#### Option B: Build Locally and Upload Static Files Yourself

If you need plugins GitHub doesn’t support:

1. Build site locally with `bundle exec jekyll build`

2. Push only the `_site` folder to a branch like gh-pages

3. Configure GitHub Pages to serve that branch

### Accessing Your Site via Default GitHub Pages Domain

Once GitHub Pages is enabled, your site will be published at:

- For user/organization site: https://username.github.io

- For project site: https://username.github.io/repository-name

GitHub takes 1–3 minutes to build the first time.

### Setting Up Custom Domains and Enforcing HTTPS

Once your site works on the default GitHub domain, you can point your own domain (like example.com) to it.

1. Buy a Domain

    - You can use any provider (Namecheap, Google Domains, Cloudflare, etc.).

2. Add the Domain in GitHub

    - Go to GitHub → Repository → Settings → Pages

    - Under Custom Domain, add: example.com

    - GitHub automatically creates a file named CNAME inside your repo to lock the domain to your site.

3. Update DNS Records

    - In your domain provider’s DNS panel (DNS changes may take up to 24 hours, usually much faster):

        | Record Type | Host | Value               |
        |-------------|------|---------------------|
        | A           | @    | 185.199.108.153     |
        | A           | @    | 185.199.109.153     |
        | A           | @    | 185.199.110.153     |
        | A           | @    | 185.199.111.153     |
        | CNAME       | www  | username.github.io  |

4. Enforce HTTPS

    - In GitHub Pages settings:

        - Check Enforce HTTPS

        - GitHub will issue a free SSL certificate via Let’s Encrypt

        - Your site will now work securely at: https://example.com