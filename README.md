# Inky
A Hugo theme with custom preferences for my blog forked from [Hugo Ink](https://github.com/knadh/hugo-ink) which itself was forked from [Ezhil](https://github.com/vividvilla/ezhil).

## Existing Features from Hugo Ink

* Syntax highlighting
* Twitter cards and opengraph tags support
* RSS feeds
* Custom CSS/JS
* Multilingual months support

## Custom Modifications

* **Removed** Google Analytics integration
* **Removed** Disqus comments
* Added the ability to set the favicon to an emoji using site params `faviconemoji`  which takes precedence over the `favicon` param
* Added the ability to set the avator to an emoji using site params `avataremoji` which takes precedence over the `avatar` image 
* Fixed tag cloud font size to be weigthed based on the total number of posts in a particular tag 
* Added Fathom Analytics which can be enabled by setting `fathomSiteId` in the site params


## Installation

cd into your hugo site's root directory and:

```sh
git submodule add https://github.com/Nial26/inky.git themes/inky
```

Note : It's important to add the theme as a submodule especially if you're using the default github pages action mentioned on [gohugo](https://gohugo.io/hosting-and-deployment/hosting-on-github/#build-hugo-with-github-action) since it fetches hugo themes from submodules 

For more information read the [official setup guide](https://gohugo.io/overview/installing/) of Hugo.


## Content type

You can specify content type with field `type` in your content. For example static pages can be set as type `page` which are excluded from recent posts and all posts page. You can use site params `mainSections` to control which page types are excluded from recent posts.

```md
---
title: "About"
date: 2019-04-19T21:37:58+05:30
type: "page"
---

This is some static page where you can write about yourself.
```

## Language Settings for the month

Due to the currently unavailable feature for multilingual dates in ``.Date`` from
Go. It is possible to create a ``month.yaml`` in the data folder of your
Hugo site root directory. There is also an example file in
``exampleSite/data/``.

```sh
cat > month.yaml << EOF
1: "Jan"
2: "Feb"
3: "Mar"
4: "Apr"
5: "May"
6: "Jun"
7: "Jul"
8: "Aug"
9: "Sep"
10: "Oct"
11: "Nov"
12: "Dec"
EOF
```

## Credits

* [Hugo Ink](https://github.com/knadh/hugo-ink)
* [Ezhil theme](https://github.com/vividvilla/ezhil) from which Hugo Ink was forked

Licensed under the MIT license.
