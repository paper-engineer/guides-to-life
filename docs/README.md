# Change log

Todo
- see if I can make it read separate collections for chapters
- figure out how to make a splash page and book landing pages...fuck it, introduction section it is, then there's just the splash page left.
- the next/prev page buttons don't work for the same reason the index.html pages don't work. fix it, then make a PR.
- it's in two locations: includes/thirdparty/chapter-list and layouts/chapter-index. so far. there may be more. 

8/2/2026
- set up the thing and made the toc work.
- copying through splash.html from minimal-mistakes did not work. or rather, it worked in the sense that I get an extra tab on my front page, but the layout didn't copy. 

---

Each chapter (section, in our book) has an index.html, it'll be fine. (it was not fine. it's broken if you use it as a project pages site with the /. whatever, I'm not using this site right now.)

use "toc: true" to generate the right pane TOC. it works if you put it under indices. now testing if it works if you put it under chapter defaults. also yes. 

using subsite to split out books works, but then literally all the chapters are in one major folder. hmmmm. 


---

# Demo site for the GitBook-inspired documentation theme for Jekyll

This is the demo site for the [GitBook-inspired documentation theme for Jekyll](https://github.com/adamrehn/jekyll-theme-gitbook). You can view the demo site live here: <https://adamrehn.github.io/jekyll-theme-gitbook-demo>.


## Legal

Copyright &copy; 2020, Adam Rehn. Licensed under the MIT License, see the file [LICENSE](https://github.com/adamrehn/jekyll-theme-gitbook-demo/blob/master/LICENSE) for details.
