# Fire and Lion

A development site for Fire and Lion (http://fireandlion.com).

## Usage

This site is built with [Jekyll](http://jekyllrb.com). Follow the installation and running instructions for Jekyll to install and run it locally.

## Editing

### Main site pages

The site's main pages (index or home page, portfolio, thinking, about, find) are markdown files in the project root.

### Portfolio

To create a new post in our portfolio, add a markdown file in `_portfolio`. It should have the following YAML frontmatter:

```
---
title: We design a new Great Expectations
excerpt: "Fire and Lion was commissioned to create a new look for Charles Dickens' classic, Great Expectations."
category: literature
image: great-expectations.jpg
order: 5
---
```

Strictly speaking, the excerpt, image and order are optional, in that the post will still appear without them; but make sure you include them for a good quality post.

The available categories are defined in _data/categories.yml`._

### Thinking posts

To create a new Thinking piece, add a markdown file to `thinking/_posts`. The file name must include the date of the post at the beginning in `YYYY-MM-DD` format, like `2017-05-15-i-love-you-indesign-but.md`.

In the file, include at least a `title`, `excerpt` and `author` in the YAML frontmatter, like this:

```
---
title: "I love you, InDesign, but it's time to let you go"
excerpt: "I love you, InDesign, but it’s time to let you go. We just can’t be together in a multi-format world."
author: Arthur Attwell
---
```

You can also include an `image` in the frontmatter, as for portfolio posts.

### Images

This site uses variously sized versions of images for different devices. To generate these, place the original, high-res versions of your images in `_source/images`, then from the Terminal or Command Prompt, in the project root (`fireandlion`), run `gulp`.

Of course, for this to work you must first install [gulp](https://gulpjs.com/).

#### Captions

To create a caption for an image, insert a markdown image inline in a paragraph, and give the paragraph the class `image-with-caption`, like this:

```
![Great Expectations]({{ site.baseurl }}/images/great-expectations.jpg)
The cover of Great Expectations
{:.image-with-caption}
```

### Drafts

You can keep unfinished drafts of posts in `_drafts`.

## Site settings

Various site settings are stored in `_data/settings.yml`, such as the site name, description, default image, canonical URL and Google Analytics Code.
