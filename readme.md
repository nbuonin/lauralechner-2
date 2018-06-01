The site is composed from one basic thing, a project, which is displayed on the site in possibly three different ways: on the homepage, on the works, and on its own distinct page.

To create a new project, create a new Markdown file in the `_projects` directory.

Each Project file starts with a set of front matter which configures how the project is displayed on the site. The complete set is:
```
---
title: "Some text goes here" 
permalink: "/url-path/"
homepage: true or false - determines if project is show on homepage
homepage-image: the name of the image you'd like to appear on the homepage
homepage-weight: the ordering of where this should be placed on the homepage
workpage: true or false - determins if the project is show on the work page 
workpage-weight: the ordering of where this should be placed on the work page 
vimeo-id: the id number from Vimeo for a video, this is used to embed the video on the work page and project page 
video-title: the title that you'd like to appear with the video
video-caption: the caption for the video 
publish-video: true or false - determines if the video is publised on the project page 
---
```

You can copy the above as the default names when creating new Projects.

Here's an explanation of each field:
`title`: Yep, you guessed it, the title that you'd like to appear
`permalink`: This is the path where the page for this project will be published, for example, "/kim/" would be published to "https://lauralechner.com/kim/"
`homepage`: this field takes either 
