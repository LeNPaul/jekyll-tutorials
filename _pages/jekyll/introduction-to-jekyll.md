---
permalink: /introduction-to-jekyll
title: "Introduction to Jekyll"
---

## What is Jekyll?

Jekyll is a static site generator that simplifies the process of building and deploying websites. Traditional dynamic content management systems (CMS) like WordPress typically rely on databases and server-side scripting. Jekyll takes page content along with template files and generates static HTML files that can be served directly by a web server, making sites faster, more secure, and easier to host.

## How Websites Work

Websites are essentially collections of files and resources that are accessed over the internet using a web browser. These files are hosted (i.e. stored) on a web server, which acts as the backend of the website. When a user requests a website through a web browser, a request is made to the web server for the website files, which are then displayed in the web browser—this acts as the frontend of the website.

Static websites consist of fixed content, meaning the web server serves the same files for every request, and each user sees the same content when they visit a website. Static websites are typically faster and simpler. Dynamic websites generate different content depending on the request. There is often server-side scripting involved, and databases are typically involved. Dynamic websites can provide personalized content, such as user accounts, but are typically slower and more complex.

What makes Jekyll useful as a static website generator is that it is able to generate an entire frontend website from content that you provide and template files. For example, you provide your blog content, and Jekyll will generate complete blog pages with headers, footers, and anything that is needed on the page. This saves time instead creating each page yourself. When you need to make a change to your website, you can make that change in one place and Jekyll will regenerate the entire website with that change.

Although static websites do not have backend server-side scripting or databases, it is still possible to utilize other services that offer features such as commenting, where your static website is making API requests to other backend web servers that manage the service for you. In many cases, this is more than enough for the majority of use cases.

## Key Features of Jekyll

###  Markdown Text Formatting

Page content is written in Markdown—a simple and popular way to format plain text—which is then automatically converted to HTML with the correct styling. Markdown is a widely used standard and allows for easy migration of content from other platforms. Markdown is essentially plain text, meaning you can store your content in a non-proprietary manner.

### Liquid Templating

Reusable layouts are built using Liquid, which is a template language used to dynamically generate pages with repeatable sections such as headers and footers. Variables can also be defined, allowing configuration changes to be applied everywhere.

### Sass Support

Sass is a CCS preprocessor that supplements CSS with useful features, such as using variables and building reusable style sheets.

### Jekyll Plugins

For features that are not directly included with Jekyll, there is a large repository of Jekyll plugins that provide many features not available out of the box with Jekyll, such as 

## Ideal Use Cases

Generally, Jekyll can be leveraged anytime you need a static website. The following are some ideas on where Jekyll can be used.

### Blogs and Portfolios 

Jekyll is blog-aware, meaning it was built with blogging in mind. You can easily generate blog pages with your content and display your blog posts in a wide variety of ways. You can also forgo the blog-specific features of Jekyll is simply create a standard portfolio website.

### Websites

Jekyll can be used build websites that don't typically require a database, such as personal or business websites. Jekyll is perfect for small organizations or business, but can also power larger sites as well. Due to the simple but fast nature of static websites, it may be ideal for websites that have a lot of traffic.

### Project Documentation

Jekyll was created by the co-founder and former CEO of GitHub, and has its roots in software development. Many software projects use Jekyll to generate project documentation. GitHub Pages, which was created for this purposes, uses Jekyll.

## Why Jekyll?

Jekyll is still relevant. Although there has been a freeze announced on the repository, releases are still being made to address bug fixes. Part of the beauty of Jekyll is that it is simple, and does exactly what it needs to do. There is no real need for significant changes to something that already works really well, and there is value in simplicity. In addition, Jekyll plugins can be used to add features that are not included with Jekyll. More importantly, GitHub continues to use Jekyll though GitHub Pages, which is widely used and even provides free web hosting, meaning Jekyll is not going anywhere soon.

For more information, visit the [official Jekyll site](https://jekyllrb.com/docs/home/) for their documentation.