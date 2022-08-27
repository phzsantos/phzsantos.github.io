---
author:
  name: Paulo Henrique Zanoteli Santos
title: Chirpy Survive Guide
date: 2022-03-09 09:50:00 UTC-3
categories: [Guides, Blog]
tags: [blog-guide]
---

## Disclaimer

This post don't replace the [official documentation](https://chirpy.cotes.page/posts/getting-started/), It's only a summary about what I think's more important.

## Change avatar picture

Create `img/avatar` inside `assets` folder

Paste the picture that you want to be your avatar picture inside `assets/img/avatar/` 

Go to `_config.yml` line 86, fill it with the image path like i did:

![Avatar](/assets/img/posts/avatar.png)

## Change favicon

Create `favicon` inside `assets/img` folder

Go to [Real Favicon Generator](https://realfavicongenerator.net/), upload your image and config it, click on *Generate your Favicons and HTML code*

Download the generated package, unzip and delete the following two from the extracted files:

- browserconfig.xml
- site.webmanifest

And then copy the remaining image files to the directory `assets/img/favicons/` 

## Run locally

First clone your repository:

```shell
git clone reponame.github.io
```

Follow [Jekyll](https://jekyllrb.com/docs/installation/) documentation to install ruby and complements

Go to the project folder, open terminal inside it and do this command:

```shell
bundle
```

**The commands above is only for the first time you're running the project locally**

Now to run a local server:

```shell
bundle exec jekyll s
```

After a while, the local service will be published at [http://127.0.0.1:4000](http://127.0.0.1:4000).

## New post structure

Folder: **_posts**

File name: **YYYY-MM-DD-TITLE.md**

Header:

```yaml
---
author:
  name: name
title: title
date: YYYY-MM-DD HH:MM:SS TTTT
categories: [cat1, cat2]        # 1 or 2
tags: [tag]                     # Always in lowercase
---
```

**Tip:** Brazillian TTTT is UTC-3.

**Tip2:** Create `posts` inside `assets/img` folder

## Official documentation

[Getting Started](https://chirpy.cotes.page/posts/getting-started/)

[Customize the Favicon](https://chirpy.cotes.page/posts/write-a-new-post/)

[Writing a New Post](https://chirpy.cotes.page/posts/write-a-new-post/)