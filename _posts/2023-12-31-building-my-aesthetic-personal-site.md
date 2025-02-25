---
layout: post
title: "Building My Aesthetic Personal Site 📝"
subtitle: "with a custom Catppuccin Jekyll theme 😺"
author: "HynDuf"
header-style: text
tags:
  - Technical
  - Ricing
---

## Inspiration 
At first, I intended to code everything from scratch but it would take so much time and I prefer having my personal site before 2024. So I decided to do some searches and came across some of the [beautiful Jekyll themes](https://github.com/topics/jekyll-theme) on Github (For anyone who doesn't know, [Jekyll](https://jekyllrb.com/) is a famous static site generator):

- [mmistakes/minimal-mistakes](https://github.com/mmistakes/minimal-mistakes)
- [alshedivat/al-folio](https://github.com/alshedivat/al-folio)
- [jekyll-theme-chirpy](https://github.com/cotes2020/jekyll-theme-chirpy)
- ...

And among those, [Huxpro/huxpro.github.io](https://github.com/Huxpro/huxpro.github.io) stood out the most as it meets some of my requirements:
- beautiful enough
- have great tags management
- post have a "Table of contents" on the sides and will follow when you scroll down

## Set up
Then, just fork and clone the repo:

- Install Ruby and Bundler. 
- Next, use `bundler install` to install all the packages listed in `Gemfile`. I got some permission errors with `bundler` and managed to fix it by install to local directory (following [Using Jekyll with Bundler](https://jekyllrb.com/tutorials/using-jekyll-with-bundler/)) (in `.gitignore` you can see a folder named `vendor`). Besides, I also got an error with package `json` not found or something, so I did something like `bundle add json` (if you use my `Gemfile`, `json` is already included).
- Then, there're 2 commands that you usually run:
    - `bundle exec jekyll serve`: To run the site to your `localhost:4000` and it has live reload too.
    - `grunt`: This is for generating the `.css` file from the `.less` file after you change some CSS. **Remember** to use the `.less` file to configure the CSS, all the `.css` files are generated from them. You can install `grunt` by `npm install grunt grunt-cli`.

## Customize
The files you typically change are in the directories `_includes`, `_layouts`, and `less`. Most of the new changes I made are in `less/hynduf.less`.

Summarizing the changes I made:
- Home page view (the banner image took up so much space, so I replaced it with some random quotes of my own).
- Added tags of posts on the home page and improved the tags' appearance.
- Changed fonts (see in `variables.less`), increased font size, and reordered many things to my liking.
- Updated Font Awesome v5 (there might be some icons that I didn't use and haven't been migrated to the new version, please create an issue if you find any).
- Github action `jekyll.yml` file that automatically build and deploy the site after committing.

### Colors
I decided to revamp the entire website with the famous [Catppuccin](https://github.com/catppuccin/catppuccin) color palette. You can see all the colors in `less/variables.less`, taken from the "Palette" section of Catppuccin.

### Dark mode
There isn't a dark mode switcher so I implemented one (and ended up refactor the color CSS). I followed [Dark Mode Revisited](https://derekkedziora.com/blog/dark-mode-revisited). You can now easily change the color to your liking in `less/variables.less` file (at the end there are sections for light and dark mode).

## Preview
Here are some previews of the website.

![home-light](/assets/home-light.png)
![home-dark](/assets/home-dark.png)
![about-light](/assets/about-light.png)
![about-dark](/assets/about-dark.png)
![archive-light](/assets/archive-light.png)
![archive-dark](/assets/archive-dark.png)
![post-light](/assets/post-light.png)
![post-dark](/assets/post-dark.png)

I think that's it. Please feel free to create any issues or contribute to the site. Special thanks to [Hux Blog](https://github.com/Huxpro/huxpro.github.io) for the incredible Jekyll theme, [Catppuccin](https://github.com/catppuccin/catppuccin) for the beautiful color palette, and a big shoutout to myself for having time to waste 😋.
