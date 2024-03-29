---
title:  "Github Pages Setup Guide"
excerpt: "Github Pages Tooltip"

categories:
  - blog
tags:
  - [blog]

toc: true
toc_sticky: true
share: false
related: false
 
date: 2022-03-21
last_modified_at: 2022-03-21

---

### :bulb:Setup

#### :one:Github.com > New 'repository'

Local clone 'repository'

if use terminal

```bash
$ git clone https://github.com/username/username.github.io
```

#### :two:New 'index.html'

```html
<!DOCTYPE html>
<html>
<body>
  <h1>Hello World</h1>
  <p>I'm hosted with GitHub Pages.</p>
</body>
</html>
```

#### :three:Commit & Sync

```bash
$ cd username.github.io
$ git add --all
$ git commit -m "Initial commit"
$ git push -u origin master
```

#### :computer:Work Test

Go 'http://username.github.io'

*reference 'https://poiemaweb.com/jekyll-basics'*

### :balloon:Jekyll Guide

```bash
$ jekyll new username.github.io
$ cd username.github.io
$ bundle install
$ bundle exec jekyll serve
```

if change '_config.yml', you must need restart serve

all done, connect http://localhost:4000 and work test.
