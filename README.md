# Top Hat

[Top Hat](https://github.com/sergiobarriel/tophat-theme) it's a simple [Hugo](https://gohugo.io/) theme just for blogging.

![screenshot](https://github.com/sergiobarriel/tophat-theme/blob/main/images/screenshot.png)

## Features

It supports:
- syntax hightlight
- featured posts
- navigation
- tags
- words count and time reading

## How to install

### Downloading files

Download .zip file from [this link](https://github.com/sergiobarriel/tophat-theme/archive/refs/heads/main.zip) and extract the content to `themes/tophat` folder

Then open your `hugo.toml` file and add the following tag:

`theme = "tophat"`

### Git submodule

Run these commands to create a Hugo site with the [tophat](https://github.com/sergiobarriel/tophat-theme) theme

```
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

```
theme = "TopHat"
title = "Your blog name"
baseURL = "https://example.com/"
languageCode = "en-us"
paginate = 5
```

The default pagination is 10 items, but you can set a different number.

### Parameters
```
[params]
  main = "post"
  featured = true
  description = "Your blog description"

  # You can customize the visibility of some elements like date, reading time, words counter and tags inside article by setting true or false
  show_date_on_article = true
  show_reading_time_on_article = true
  show_words_count_on_article = true
  show_tags_on_article = true  
```

### Menus

```
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

```
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

## CSS / SCSS Styles

There are some `scss` files inside `assets/scss` folder, so you can customize the styles as you wish and then transpile by using [sass](https://sass-lang.com/dart-sass/) command

`sass styles.scss ../css/styles.css`
