# Rename This Theme Please

A basic website template for Jekyll. Browse through a [live demo](https://brave-submarine.cloudvent.net/).

![Frisco template screenshot](images/_screenshot.jpg)

The [original Frisco](https://github.com/CloudCannon/frisco-jekyll-template) was made by [CloudCannon](http://cloudcannon.com/). I have refactored it for extendability and best practices. 

I believe this has pretty much ended up looking like a less sophisticated reskin of [Forty](https://andrewbanchich.github.io/forty-jekyll-theme/), although obviously it's a little different under the hood. I might mess with that one too, at some point. 

## Features

* Contact form (note: I didn't test this!)
* Pre-built pages
* Pre-styled components
* Blog with pagination
* Post category pages
* Disqus comments for posts (note: I didn't test this)
* Staff and author system
* Configurable footer
* RSS/Atom feed
* SEO tags (note: I didn't test this)
* Google Analytics (note: I didn't test this)

## Setup

0. Clone or fork or whatever, I cbf with remote themes. 
1. Add your site and author details in `_config.yml`. 
2. Add your Google Analytics and Disqus keys to `_config.yml`. (note: I didn't test this)
3. It should just work out-of-the-box with GH Pages once your url and baseurl are correct. I am...pretty sure Cloudflare Pages and other such sites will be fine too. And if you've gotten to the point of actually downloading Jekyll, then you're further into it than I am and I believe in your ability to make it work. 

## Develop

The original Frisco was built with [Jekyll](http://jekyllrb.com/) version 3.3.1. It seems to currently still work on github pages as of 2026. As it's under the MIT license, you should keep messing with it if it's unsatisfactory. 

The javascript that manages the top navigation bar light/dark toggle is, according to chatgpt, outdated. Considering where I got the original from, no surprise. But it works right now. 

Install the dependencies with [Bundler](http://bundler.io/):

~~~bash
$ bundle install
~~~

Run `jekyll` commands through Bundler to ensure you're using the right versions:

~~~bash
$ bundle exec jekyll serve
~~~

## Editing

I feel like _data, _pages, _posts, _staff_members, _images are pretty self-explanatory. The CloudCannon editing functionality was removed. Sorry guys. 

### Posts

* Add, update or remove a post in the *Posts* collection.
* The **Staff Author** field links to members in the **Staff Members** collection.
* Documentation pages are organised in the navigation by category, with URLs based on the path inside the `_docs` folder.
* Change the defaults when new posts are created in `_posts/_defaults.md`.

(I didn't do anything to this)

### Contact Form

* Preconfigured to work with CloudCannon, but easily changed to another provider (e.g. [FormSpree](https://formspree.io/)).

(I didn't do anything to this)

### Staff

* Reused around the site to save multiple editing locations.

### Top Navigation Bar

* Exposed as a data file to give clients better access.
* Set in the *Data* / *Navigation* section.

### Footer

* Exposed as a data file to give clients better access.
* Set in the *Data* / *Footer* section.
