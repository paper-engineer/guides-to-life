# Change log

Todo1:
- my actual remaining next step is to put up the logo, clean up the pages and content, and do dns
- I would like to migrate to cloudflare pages at some point, I think

Todo2:
- we're sufficiently done that I think my next step with the template is actually to clone it out, polish it and publish it. which, okay, is actually never happening. not with the amount of documentation I'd have to write. but the option is there. 

19/4/2026: successfully hacked frisco by...a lot...

it's no longer frisco, I can just fucking finish documenting and release it as new. it's basically forty but with, like, less polish. 

18/4/2026: lol landing-page is actually a single page theme, but I need like 4 pages. rip. it works but is insufficient. would have to hack it anyway, but even so. 
changed to frisco theme instead and now trying to hack that. first make it best-practice-consistent, then start futzing with content and layout. 

(we assume the content is fixable later, this log is for functionality)

okay, honestly, at this point, the thing to do is probably fork minimal-mistakes and tack-on the nav pane stuff, making it iterate in alphabetical order. also the css, just because. 

(the thing to do was find a book theme and make each book a separate subsite, and the main site just has a landing page with links out)

okay I think we'll just use this one for the books landing page
https://github.com/swcool/landing-page-theme
guess I put that up now somehow

suits the laser
https://github.com/a-chacon/wind
https://chrisanthropic.github.io/starving-artist-jekyll-theme/documentation/layouts/
https://github.com/abhinavs/moonwalk
https://github.com/jeromelachaud/freelancer-theme
https://github.com/sharu725/bheema
https://github.com/sharu725/karna
https://github.com/BGMP/bgm.dev
https://github.com/CloudCannon/fur-jekyll-template

maybe suits the laser
https://github.com/vvalchev/creative-theme-jekyll-new
https://github.com/chrisbobbe/jekyll-theme-prologue
https://github.com/sharu725/cards
https://github.com/willianjusten/cards-jekyll-template
https://github.com/fu4303/photography-aperature

now with a repository here of weirdies or potentially useful sites that I think to keep
https://github.com/thiagorossener/jekflix-template
https://github.com/hunvreus/carte
https://github.com/SriSatyaLokesh/theprofile
https://github.com/joaomlneto/jekyll-multiverse-template
https://hydejack.com/
https://andrewbanchich.github.io/forty-jekyll-theme/
https://github.com/olivier3lanc/Jekyll-LibDoc
https://github.com/CloudCannon/cause-jekyll-template
https://github.com/CloudCannon/frisco-jekyll-template
https://github.com/dashingcode/front-cover
https://github.com/CloudCannon/aviator-jekyll-template
https://github.com/emilbaehr/automatic-app-landing-page

Todo
- see if I can make it read separate collections for chapters
- raise an issue about the page.url and index.baseurl thing, fork the project if it doesn't work. refer logs 8/2/2026

8/2/2026
- set up the thing and made the right pane toc work.
- copying through splash.html from minimal-mistakes did not work. or rather, it worked in the sense that I get an extra tab on my front page, but the layout didn't copy. 
- the next/prev page buttons don't work on project pages, it's missing a |index.baseurl| somewhere in the code. 
- it's in multiple locations in multiple ways:
  - includes/thirdparty/chapter-list (fixable by adding |index.baseurl|) 
  - layouts/chapter-index (page.url is a different beastie but this one has been fixed too)
  - includes/internal/prev-next.html (uses previous.url and next.url and I can't figure out the fix) it had relative_uri, which, what. 
  - according to chatgpt, relative_url already prepends the baseurl so it should have already worked. 
- well, it'll resolve itself when there's a website. hopefully? or we can raise an issue. 
- also I got a splash page (almost) working, got chatgpt to make the splash page more jekyll-like, and now we're onto chatgpt customisations. why not.
- it's now splashed fine, but not reading separate collections, and I think the collections experiment broke my left pane (manually went to address to check)

---

Each chapter (section, in our book) has an index.html, it'll be fine. (it was not fine. it's broken if you use it as a project pages site with the /. whatever, I'm not using this site right now.)

use "toc: true" to generate the right pane TOC. it works if you put it under indices. now testing if it works if you put it under chapter defaults. also yes. 

using subsite to split out books works, but then literally all the chapters are in one major folder. hmmmm. 

header/footer include hooks work, as default

book landing pages use a section "0-introduction"

---

# Demo site for the GitBook-inspired documentation theme for Jekyll

This is the demo site for the [GitBook-inspired documentation theme for Jekyll](https://github.com/adamrehn/jekyll-theme-gitbook). You can view the demo site live here: <https://adamrehn.github.io/jekyll-theme-gitbook-demo>.


## Legal

Copyright &copy; 2020, Adam Rehn. Licensed under the MIT License, see the file [LICENSE](https://github.com/adamrehn/jekyll-theme-gitbook-demo/blob/master/LICENSE) for details.

---

# Landing Page Jekyll theme

Jekyll theme based on [landing-page bootstrap theme ](http://startbootstrap.com/templates/landing-page/)

## How to use
 - Place a image in `/img/services/`
 - Create posts to display your services. Use the follow as an example:

```txt
---
layout: default
img: ipad.png
category: Services
title: The service title
---
The description of this service
```

## Demo
View this jekyll theme in action [here](https://swcool.github.io/landing-page-theme)

## Screenshot
![screenshot](https://raw.githubusercontent.com/swcool/landing-page-theme/master/img/screenshot.png)

===

For more Jekyll details, read [documentation](http://jekyllrb.com/).
This Jekyll theme used [Freelancer Jekyll theme](https://github.com/jeromelachaud/freelancer-theme/) as reference.

## License
The contents of this repository are licensed under the [Apache
2.0](http://www.apache.org/licenses/LICENSE-2.0.html).

## Version
1.0.1
