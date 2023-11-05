# Top Hat

[Top Hat](https://github.com/sergiobarriel/tophat-theme) it's a simple [Hugo](https://gohugo.io/) theme just for blogging.

![screenshot](https://raw.githubusercontent.com/sergiobarriel/tophat-theme/main/images/screenshot.png)

## Live view

My own blog [nohat.dev](https://www.nohat.dev) uses this theme

## Features

It supports:
- syntax hightlight
- featured posts
- navigation
- tags
- words count and time reading

## How to install

You can use the theme in by two flavors, [downloading files from repository](#download-files-from-repository) or [using git submodule ](#use-git-submodule)

### Download files from repository

Download .zip file from [this link](https://github.com/sergiobarriel/tophat-theme/archive/refs/heads/main.zip) and extract the content to `themes/tophat` folder

Then open your `hugo.toml` file and add the following tag:

`theme = "tophat"`

### Use git submodule

Run these commands to create a Hugo site with the [tophat](https://github.com/sergiobarriel/tophat-theme) theme

```shell
hugo new site my-blog
cd my-blog
git init
git submodule add https://github.com/sergiobarriel/tophat-theme.git themes/tophat
echo "theme = 'tophat'" >> hugo.toml
hugo server
```

If you want to update the theme with the latest changes just run the command

`git submodule update --remote`

## How to configure the theme

### Options

You should configure minimal options on your `hugo.toml` file:

```toml
theme = "TopHat"
title = "Your blog name"
baseURL = "https://example.com/"
languageCode = "en-us"
paginate = 5
```

The default pagination is 10 items, but you can set a different number.

### Parameters
```toml
[params]
    
  subtitle = "Your blog subtitle"
  description = "Your blog description"
  author = "Sergio Barriel"

  main = "post"
  featured = true
  
  # You can customize the visibility of some elements like date, reading time, words counter and tags inside article by setting true or false
  show_date_on_article = true
  show_reading_time_on_article = true
  show_words_count_on_article = true
  show_tags_on_article = true  
```

### Menus

```toml
[menu]

  [[menu.main]]
    identifier = "about"
    name = "About"
    url = "/pages/about/"

  [[menu.main]]
    identifier = "contact"
    name = "Contact"
    url = "/pages/contact/"    
  
  [[menu.social]]
    identifier = "twitter"
    name = "Twitter"
    url = "https://twitter.com/sergiobarriel" 

  [[menu.social]]
    identifier = "github"
    name = "Github"
    url = "https://github.com/sergiobarriel"

```

### Google Analytics

If you want to track telemetry from Google Analytics just add the `googleAnalytics` tag on your hugo.toml file

`googleAnalytics = "G-XXXXXXXXXX"`

### Syntax highlight

You can customize the highlight configuration by overriding options on hugo.toml file according to these [params](https://gohugo.io/getting-started/configuration-markup/#highlight)

```toml
[markup]
  [markup.highlight]
    anchorLineNos = false
    codeFences = true
    guessSyntax = false
    hl_Lines = ''
    hl_inline = false
    lineAnchors = ''
    lineNoStart = 1
    lineNos = false
    lineNumbersInTable = true
    noClasses = true
    noHl = false
    style = 'dracula'
    tabWidth = 4
```

See the [Style Gallery](https://xyproto.github.io/splash/docs/all.html#friendly) for a full overview of available styles and how they may appear.

## Customize styles

There are some `scss` files inside `assets/scss` folder, so you can customize the styles as you wish and then transpile by using [sass](https://sass-lang.com/dart-sass/) command

`sass styles.scss ../css/styles.css`

## Sponsor

If you like the project, you can consider making a donation at [ko-fi.com](https://ko-fi.com/sergiobarriel)

## Contributors / Collaborators

These individuals have contributed to the repository through suggestions, error corrections, or by opening issues. Thanks 😊

- [foldfree](https://github.com/foldfree)
- [christian-cell](https://github.com/christian-cell)

## Support

You can contact me via Twitter [@sergiobarriel](https://twitter.com/sergiobarriel), or if you have an [issue](https://github.com/sergiobarriel/tophat-theme/issues), you can open one 🙂
