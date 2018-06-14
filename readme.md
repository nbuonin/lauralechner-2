## Overview
The site is composed from two basic types: projects, and blog posts. These types are displayed in a few possible ways.  Projects are rendered on the homepage, on the works page, and on its own distinct page. Blog posts have a listing page, are listed on the related project page, and its own page.


The site uses Markdown for styling content. A quick guide to Markdown can be found [here](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet).


Some creative folks have made online Markdown editors which you can use to draft your posts, and then paste into Github:
- [Minalimist Editor](http://markdown.pioul.fr/)
- [StackEdit](https://stackedit.io/app#) This can also connect to your Github account. In my experience these can be hard to manage. Each save creates a new commit, which makes the commit log useless.

## Markdown Basics
Each Markdown file starts with front matter. Front matter consists of key-value pairs of settings for that particular post.  For example: `title: "My Amazing Title"` would set the title of the post to "My Amazing Title". Front matter need to start on the first line of a file; it starts and ends with three dashes: `---`.


The values in front matter have implicit types: i.e strings of text, numbers, dates, true/false. In many cases Jekyll can infer the type of value just fine, but it will sometimes get tripped up on strings of text. Though its not actually required, I'd suggest wrapping strings of text in single or double quotes. If you're ever unsure of what to do, you can refer to existing posts.

The content of the post follows the front matter, and its here where you can use Markdown syntax to style your text.  You can also use HTML here if you need to, like embedding a video. One common gotcha with Markdown is line spacing.  To get a single line space between paragraphs, you need to enter two new lines in the Markdown file.


## How to Create a Project
1. Create a new Markdown file in the `_projects` directory.
2. Copy in the front matter and replace the help text with actual content:
```
---
title: "Some text goes here" 
permalink: "/url-path/" This is the path where the page is published, for example, "/kim/" would be published to "https://lauralechner.com/kim/". Avoid using "/blog/" as that will collide with blog posts
homepage: true or false - determines if project is shown on homepage
homepage-image: the file name of the image that you'd like to appear on the homepage
homepage-weight: the ordering of where this should be placed on the homepage
workpage: true or false - determines if the project is shown on the work page 
workpage-weight: the ordering of where this should be placed on the work page 
vimeo-id: the id number from Vimeo for a video, this is used to embed the video on the work page and project page 
video-title: the title that you'd like to appear with the video
video-caption: the caption for the video 
publish-video: true or false - determines if the video is publised on the project page 
project-tag: Use this tag to associate blog posts with a specific project 
---
```
3. Fill in your content

## How to Create a Blog Post
1. Create a new Markdown file in the `_blog` directory.
2. Copy in the front matter:
```
---
title: "Title goes here"
date: 2016-07-01
project-tag: "kim"  
blog-image: "fromtheheartlogo.png"
---
```
3. Fill in your content


## Images
Images can be uploaded directly to Github, and saved to the `images` folder. Its best not to have spaces in file names, its better to use underscores instead.

When specifying an image in your front matter, you can refer to it using only the file name, like in the examples above.

But your not limited to using images only in the front matter.  Images can be added to posts using Markdown, like so:
`![alt text]({{ "/images/filename.jpg" | absolute_url }} "Title ext appears on hover")`

Note the funny stuff in the curly braces. This is a Jekyll filter that makes sure that the correct path is set for the image. More info about this can be found [here](https://jekyllrb.com/docs/posts/#including-images-and-resources)

