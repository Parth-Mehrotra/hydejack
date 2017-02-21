# How to use your new blog platform: 

## Features
Features include:

* Touch-enabled sidebar / drawer for mobile, including fallback when JS is disabled.
* Github Pages compatible tag support based on [this post][tag].
* Customizable link color and sidebar image, per-site, per-tag and per-post.
* Optional author section at the bottom of each post.
* Optional comment section powered by Disqus.
* Layout for posts grouped by year
* Wide array of social media icons on sidebar.
* Math blocks via [KaTeX](https://khan.github.io/KaTeX/).


## Manual

### Configuration
You can configure important aspects of the theme via [`_config.yml`]
(https://github.com/Lattice3f/blog/blob/gh-pages/_config.yml). This includes:

* the blog description in the sidebar
* the (optional) author description and photo
* default image and link color of the blog
* the current github name (you can include various other social media platforms)

### How to Change the Image and Color of a Post
In the manifest of a blog post, simply add an url as `image` and a CSS color as `color`:

~~~yml
layout: post
title: Introducing Hydejack
image: http://qwtel.com/hydejack/public/img/hyde.jpg
color: '#949667'
~~~

### How to Add a New Tag
Tags are possible, but they are not meant to be used #instagram #style: #food #goodfood #happy #happylife #didimentionfood #yougetthepoint. Each tag requires some setup work. I tend to think of it as categories that can be combined.

1.  Add an entry to `_data/tags.yml`, where the key represents a slug and provide at least a `name` value and optionally `image`, `color` and `description`.

    Example `/_data/tags.yml`:

    ~~~yml
    mytag:
      name: My Tag
    ~~~

2.  Make a new file in the `tag` folder, using the same name you've used as the key / slug and change the `tag` and `permalink` entries.

    Example `/tag/mytag.md`:

    ~~~yml
    layout: blog-by-tag
    tag: mytag
    permalink: /tag/mytag/
    ~~~

3.  Tag your blog posts using the `tags` key (color and image will only depend on the first tag).

    ~~~yml
    layout: post
    title: Introducing My New Tag
    tags: [mytag, othertag]
    ~~~

4. Add the tag to the sidebar, by adding it to `sidebar_tags` in `_config.yml`.
   They will appear in the listed order.

   ~~~yml
   sidebar_tags: [mytag, othertag]
   ~~~
### How to Add a New Post

1. Got to [`_posts`](https://github.com/Lattice3f/blog/tree/gh-pages/_posts) and create a new file.

2. The file name should follow this format: (YYYY-MM-DD-postname.md)
    this will ensure the post are presented in chronological order.
    
3. Always have this at the top of the post to ensure the post is tagged correctly:
```
---
layout: post
title: 
tags: []
---
```
Here's an example:

```
---
layout: post
title: Recursion
tags: [algorithms]
---
```
4. Refer to this [cheatsheet](https://guides.github.com/features/mastering-markdown/) to insert images, links, etc.

### How to Change the About Information
1. You can configure part of your about page here, including image: via [`_config.yml`](https://github.com/Lattice3f/blog/blob/gh-pages/_config.yml)

2. While you can include all the information you want from the link above, you can include additional information via: [`_about.md`](https://github.com/Lattice3f/blog/blob/gh-pages/about.md) 
