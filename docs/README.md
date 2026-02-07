# Change log

Todo
- see if I can make it read separate collections for chapters
- figure out how to make a splash page
- ugh, and the faq/website design stuff, but that's basically just a book and some hooks. 
- raise an issue about the page.url and index.baseurl thing

8/2/2026
- set up the thing and made the toc work.
- copying through splash.html from minimal-mistakes did not work. or rather, it worked in the sense that I get an extra tab on my front page, but the layout didn't copy. 
- the next/prev page buttons don't work on project pages, it's missing a |index.baseurl| somewhere in the code. 
- it's in multiple locations in multiple ways: includes/thirdparty/chapter-list (fixable by adding |index.baseurl|) and layouts/chapter-index (page.url is a different beastie). 
- found one in includes/internal/prev-next.html that uses previous.url and next.url
- well, it'll resolve itself when there's a website. hopefully? or we can raise an issue. 
- the page.url one fixed itself, so maybe hopefully I rebuild a page and it'll pull the new prev-next?
- nope, it didn't. 
- also I got a splash page working, now to make it fucking behave
- got chatgpt to make the splash page more jekyll-like, and we'll see if it works

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
