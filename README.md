# Zer0TrustSec

Welcome to my Zer0TrustSec project! This README will guide you through the process of setting up, running locally, and deploying on GitHub Pages.

## Installation

To run this Jekyll project locally, follow these steps:

1. **Clone the Repository:**

   ```bash
   git clone https://github.com/NoorShaik683/zer0TrustSec_website.git
   cd your-repo
   ```
2. **Install Jekyll:**
   
   Ensure you have Ruby and RubyGems installed on your system. Then, install Jekyll and Bundler if you haven't already:

   ```bash
   gem install jekyll bundler   
   ```

3. **Install Dependencies:**
   
   Install project dependencies using Bundler:

   ```bash
      bundle install   ```

4. **Serve the Site:**

   Start the local development server:

   ```bash
   bundle exec jekyll serve
   ```
   Your site will be available at http://localhost:4000. You can view it in your web browser.

## Usage
   
   Modify and customize the project to create your own website. Edit content, layouts, and styles in the _posts, _layouts, and _sass directories, among others.

## Deployment to GitHub Pages

To deploy your Jekyll site to GitHub Pages, follow these steps:

1. **Create a GitHub Repository:**
   
Create a new GitHub repository with the name <yourusername>.github.io. This naming convention is required for GitHub Pages.

2. **Configure Your Repository:**
   
In your project directory, open the _config.yml file and set the url field as follows:

   ```yaml
   url: https://<yourusername>.github.io
   ```

3. **Build Your Site:**
   
Build your Jekyll site for production:

   ```bash
   bundle exec jekyll build
   ```

4. **Push to GitHub:**

Push the generated _site directory to your GitHub repository:

   ```bash
   git add _site
   git commit -m "Add Jekyll site files"
   git push origin master
   ```

5. **GitHub Pages Settings:**
   
In your GitHub repository, go to "Settings" > "Pages." Choose the "master branch" as the source and click "Save." Your site will be available at https://<yourusername>.github.io.   



# Writing a New Post Guide

This guide will help you write and format your posts in the Chirpy Jekyll template. Whether you're new to Jekyll or have experience, this guide covers important details and best practices for creating your content.

## Naming and Path

To create a new post, follow these naming and path conventions:

- Create a new file named `YYYY-MM-DD-TITLE.EXTENSION` (e.g., `2023-09-27-my-post.md`).
- Place the file in the `_posts` directory at the root of your project.
- The file extension must be either `.md` or `.markdown`.

If you want to streamline file creation, consider using the Jekyll-Compose plugin.

## Front Matter

Every post requires Front Matter at the top. Here's an example:

```markdown
---
title: TITLE
date: YYYY-MM-DD HH:MM:SS +/-TTTT
categories: [TOP_CATEGORY, SUB_CATEGORY]
tags: [TAG]     # TAG names should always be lowercase
---
```
The layout for posts is set to "post" by default, so you don't need to add the layout variable in Front Matter.

## Timezone of Date

For accurate post timestamps, set the timezone in the date variable like this: +/-TTTT, e.g., +0800. Also, configure the timezone in _config.yml.

## Categories and Tags
 
 Each post can have up to two categories and an unlimited number of tags. Example:

   ```markdown
---
categories: [Animal, Insect]
tags: [bee]
---
```

## Author Information

By default, author information is obtained from _data/authors.yml. To override it, add author details to the YAML block:

   ```yaml
author: <author_id>                     # for single entry
# or
authors: [<author1_id>, <author2_id>]   # for multiple entries
   ```

## Table of Contents

Enable or disable the Table of Contents (TOC) globally in _config.yml. For specific posts, use:

   ```markdown
---
toc: false
---
   ```

## Comments

Configure global comments settings in _config.yml. Disable comments for specific posts with:

   ```markdown
---
comments: false
---
```

## Mathematics

Enable mathematical notation:

   ```markdown
---
math: true
---
```

## Mermaid

Enable Mermaid diagrams:

   ```markdown
---
mermaid: true
---
```

## Images

   Caption
   Add image captions by italicizing the next line of the image:

   ```markdown
![img-description](/path/to/image)
_Image Caption_
```

## Size

Set width and height for images to prevent layout shifts:

   ```markdown
![Desktop View](/assets/img/sample/mockup.png){: width="700" height="400" }
   ```

## Position

   Specify image position (normal, left, right):

   ```markdown
![Desktop View](/assets/img/sample/mockup.png){: .normal }
![Desktop View](/assets/img/sample/mockup.png){: .left }
![Desktop View](/assets/img/sample/mockup.png){: .right }
```

## Dark/Light mode

   Make images follow theme preferences in dark/light mode:

   ```markdown
![Light mode only](/path/to/light-mode.png){: .light }
![Dark mode only](/path/to/dark-mode.png){: .dark }
```

## Shadow
   Add a shadow effect to images:
   ```markdown
![Desktop View](/assets/img/sample/mockup.png){: .shadow }
```

## CDN URL

   If using a CDN, set the img_cdn variable in _config.yml:

   ```yaml
   img_cdn: https://cdn.com
```
The CDN URL will be automatically added to image paths.

## Image Path

Define a common image path in the post's YAML block:

   ```yaml
---
img_path: /img/path/
---
```

Then, use image file names directly:

   ```markdown
![The flower](flower.png)
```

## Preview Image

Add a top-of-the-post image with resolution 1200 x 630:

   ```yaml

---
image:
     path: /path/to/image
     alt: image alternative text
---
```

## LQIP (Low-Quality Image Placeholder)

For preview images:

   ```yaml
---
image:
     lqip: /path/to/lqip-file # or base64 URI
---
```

## Pinned Posts

Pin posts to the top of the home page:

   ```yaml

---
pin: true
---
```

## Prompts

Use prompts (tip, info, warning, danger) by adding the corresponding class to a blockquote:

   ``` markdown

> Example line for prompt.
{: .prompt-info }
```

## Syntax

   Inline Code: inline code part

   Filepath Highlight: /path/to/a/file.extend{: .filepath }
   
   Code Block: Use triple backticks (```)

Specify the language for syntax highlighting:

```yaml
key: value

```
## Line Number

Hide line numbers for a code block with the .nolineno class:

   ``` shell

echo 'No more line numbers!'
{: .nolineno }
```

## Specifying the Filename

Replace the code language with the file name using the file attribute:

   ```shell
# content
{: file="path/to/file" }
```

