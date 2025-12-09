## Discontinued!

<img style="border-radius: 20px;" src="https://i.imgur.com/nyoM6z6.png">

# FalixNodes Help Center
What's all this? You're currently viewing the source code that makes up the [help center](https://help.falixnodes.net/). It's all built on Jekyll, a static website generator we use for a couple of our sites.

We're using our own template built and designed by our partner [Korbs Studio](https://github.com/KorbsStudio/).

![Powered by Jekyll](https://img.shields.io/badge/powered_by-Jekyll-blue.svg) ![Website Build - VPS](https://github.com/FalixNodes-Software/help-center/actions/workflows/jekyll-build.yml/badge.svg)

# Creating a New Article
Want to help contribute to the Help Center? Write or update an article!

## 🛡️ Requirements 
 - The communication must be clear and well explained for the user to understand
 - Fact check and make sure the information you're providing is accurate
 - Good grammar [Check out QuillBot](https://quillbot.com/grammar-check)
 - Valid syntax
 - Proper metadata
 - Valid links and up to date

## ✍️ Creating an Article
By following the file structure, create a `.md` file under the correct category. As an example, if you were to create an article that explains on how to install and use a plugin on Minecraft Java, the file would be created like `_posts_/minecraft/plugins/2021-08-04-plugin-name.md`. You're required to add the date at the beginning of the file name, `YYYY-DD-MM`. These dates are used to show when the article was last updated, to allow users to know if the article is up to date.

 Then start writing the article in [Markdown](https://www.markdownguide.org/getting-started/). Writing in Markdown is very easy to do, if you need help understanding how to do certain task like creating a link, inserting an image, creating a list look [here](https://guides.github.com/features/mastering-markdown/).

## 📃️ Metadata
Make sure the metadata is setup properly, this is usually at the top of every article.
It should look like this:
```
---
layout: post
title:  "Title of Article"
categories: Minecraft
tags: plugins
icon: <i class="fa-light fa-file-user"></i>
permalink: /minecraft/plugins/name-of-plugin/

author: Username
authorGitHub: username
---
```

`layout` must remain as `post`.

`tags` is the sub-category.

`icon` - When viewing our help center, an icon is displayed by each article link. Use the default one if you're unsure what icon to use.

Default: `<i class="fa-light fa-file-user"></i>`

Getting Started Articles: `<i class="fa-light fa-wand-magic-sparkles"></i>`

Plugins: `<i class="fa-light fa-puzzle"></i>`

Discord JavaScript: `<i class="fa-brands fa-js-square"></i>`

Discord Python: ` <i class="fa-brands fa-python"></i>`

BungeeCord: `<i class="fa-light fa-diagram-project"></i>`

> Icons are provided by Font Awesome

> If the article does not contain any metadata or at least valid ones, the help center will not show the article anywhere.

> If you're adding a new category, contact __Korbs#0001__ right away so he can setup a section for it.

## Content
### Plugin's Download
At the top of each plugin article, there is a box displays information about the plugin with a download link, example:

<img src="https://i.imgur.com/KsS4RAB.png">

If you plan to create an article explaining how to use a plugin, it's best you use this at the top of the article. The code is:
```
<div class="install-plugin">
    <img style="border-radius: 7px;" src="#">
    <h2>Name of Plugin</h2>
    <h3>Developer: Author</h3> 
    <a href="#">Download this Plugin</a>
</div>
```

### Headers
Uisng "# Title of Article" isn't needed, the layout will automatically add the title of the article to the top of the webpage.

## Header 2
```
## Header 2
```

### Header 3
```
### Header 3
```

#### Header 4
```
#### Header 4
```

### Links
[FalixNodes](https://falixnodes.net/)
```
[FalixNodes](https://falixnodes.net/)
```

### List and Check Lists
List:
 - Item
 - Item
 - Item
 - Item
```
 - Item
 - Item
 - Item
 - Item
```

### Tables
A table is used to display content clearly without making a mess, like we did in the [Getting Started](https://help.falixnodes.net/minecraft/general/getting-started/#message-of-the-day) article under Minecraft, showing a color code table.

Example: 

| Example        | List          |
|:---------------|:--------------|
| Example        | Content       |
| Example        | Content       |
| Example        | Content       |
| Example        | Content       |

Code:
```
| Example        | List          |
|:---------------|:--------------|
| Example        | Content       |
| Example        | Content       |
| Example        | Content       |
| Example        | Content       |
```

### Video
I personally like seeing `<video>` in the help center over a YouTube embed, but you're allowed to use a YouTube embed if you want to.
[Learn how to embed a YouTube video](https://support.google.com/youtube/answer/171780?hl=en)

```
<video controls preload="auto"><source
 src="https://example.com/video.webm" type="video/webm"
 src="https://example.com/video.mp4" type="video/mp4"
 /></video>
```
If you're adding a video to the files, use a path like `/assets/videos/etc/etc/etc`.

Make sure to provide both webm and mp4. Webm are much smaller and load faster, although an MP4 file is required as not all browsers support webm format. So the MP4 is more of a fallback option if the user's browser doesn't like the webm format.

## 📢️ Publishing
Create a pull request on this repo and title it like this "New Post: Name of Article" or if you're editing an article, title it like "Edit: Name of Existing Article".

Your edit will be reviewed by our support team along with your code to check for any syntax error.

# Building
If you're interested in learning on how to build the Help Center locally, maybe to preview that your article does show up properly, just follow the instructions below.

Since the Help Center is powered by Jekyll, you'll need to install [Ruby](https://www.ruby-lang.org/en/) for your operating system.
 - [Download for Windows](https://rubyinstaller.org/)
 - [Download for macOS](https://www.ruby-lang.org/en/downloads/)

### Installing Ruby on Linux
Debian/Ubuntu:
```
sudo apt-get install ruby-full build-essential zlib1g-dev
gem install jekyll bundler
bundle install
```
Fedora/RedHat:
```
sudo dnf install make automake gcc gcc-c++ kernel-devel ruby-devel
gem install jekyll bundler
bundle install
```

## Building and Locally Hosting

To run a localhost server, run:
```
bundle exec jekyll serve
```

Howerver, the development mode pulls from a different source with CSS, you'll need to clone the main website for that. Open the terminal in the main website repo, and run:
```
bundle exec jekyll serve --port 4003
```

After using `bundle exec jekyll serve`, try going to http://localhost:4000/ in your preferred web browser.

If you're unable to get Ruby installed or the serve command working, you can always resort to building it on other platform like GitHub Pages, Cloudflare Pages, or Netlify.

___
> All PRs are closed if inactive for a long period of time, usually about 3 weeks to a month.

