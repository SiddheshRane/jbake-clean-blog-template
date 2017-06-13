# Clean Blog JBake Theme 

A port of Clean Blog by Start Bootstrap for JBake

## Features

- Fully functional **out of the box**. No need to modify templates for trivial customization.
  Individual specific customization goes in `jbake.properties`
- Post **snippet** instead of full post in index. The snippet is taken as the first paragraph (`<p>` element) from post body
- **Tag list** with links to tag page in index and post
- Navbar **auto lists `pages`** using `page.title` and `page.uri`
- **Github**, **Twitter**, **Linkedin** links at the footer
- Uses thymeleaf the way it was intended to be used. This means you can **preview** the theme even **before baking** it

## Missing  

- No pagination support as yet. If you set `index.paginate=true` in `jbake.properties` 
you'll have multiple index files in the sequence `index.html`, `index0.html` ... by JBake but the theme
doesn't do anything to link these pages
- No disqus comments yet
- No google analytics yet
- Currently nothing links to the archive page. Will fix that soon
- Navbar auto lists all pages by default. This is fine if you have few important pages like about and contact
  but if there are a lot of pages that are not top level, but can be reached from other pages, then it becomes
  messy. I plan to introduce custom metadata for indicating whether a page should be  *pinned* or not

## How to use

Download this repo to your system.
I assume you are familiar with JBake and have installed it on your system.

If you already have a blog
- replace your `templates` folder with this one.
- Remove your earlier theme specific files from `assets`.
- copy files from my `assets` folder to your `assets` folder.
- Copy contents from my `jbake.properties` file to your `jbake.properties` file.
  Replace overlapping entries.
**NOTE:** This theme sets output folder to `docs` by default.

If you wish to start from scratch with this theme:
- Remove unwanted files like README, LICENSE, `nbproject`. this step is optional though
- modify user/blog specific fields in `jbake.properties`
- Delete sample files from contents folder, or modify them to start with your content

Finally `jbake -b` to render your site. 