![screenshot](https://raw.githubusercontent.com/dim0627/hugo_theme_solit/master/images/screenshot.png)

# What is this.

This is the theme for Hugo that supports the [Accelerated Mobile Pages Project](https://www.ampproject.org/).

[Hugo :: A fast and modern static website engine](https://gohugo.io/)

# Features

* [Accelerated Mobile Pages Project](https://www.ampproject.org/) a.k.a AMP supported.
* Responsive Design
* Google Analytics.
* Thumbnail.
* High score by Google Page Speed Insight.
* Share button.
* Structured data(Article and Breadcrumb).
* Twitter cards.
* OGP
* Optimized for SEO.

# Config example

```
baseurl = "https://example.com/"
title = "SiteTitle"

googleAnalytics = "UA-XXXXXXXX-XX" # Optional

[params]
  contact = "contact@example.com" # Optional
  # Fonts settings.
  googlefonts = "https://fonts.googleapis.com/css?family=Lobster|Lato:400,700" # Optional, Include google fonts.
  fontfamily = "Lato,游ゴシック体,'Yu Gothic',YuGothic,'Hiragno Sans','ヒラギノ角ゴシック Pro','Hiragino Kaku Gothic Pro',メイリオ,Meiryo,sans-serif" # Optional, Override body font family.
  logofontfamily = "Lobster, cursive" # Optional, Override logo font.
```

# Frontmatter example

```
+++
date = "2016-09-28T17:00:00+09:00"
title = "Article title here"
thumbnail = "thumbnail.jpg" # Optional, referenced at `$HUGO_ROOT/static/images/thumbnail.jpg`
+++
```

# Recommends directory structure

This themes `Header Menu` is using section.
Recommend that you use the section than taxonomy.

```
.
├── config.toml
├── content
│   ├── section1         # Separated by section.
│   │   └── article1.md
│   └── section2
│       └── article2.md
├── layouts
└── static
    ├── favicon.ico
    └── images           # Place here thumbnail images.
        └── thumbnail.png
```

# Shortcodes

## Iframe

```
{{% iframe src="https://www.youtube.com/embed/XXXXXXX" w="560" h="315" %}}
```

## Image

```
{{% img src="/images/image.jpg" w="600" h="400" %}}
{{% img src="/images/image.jpg" w="600" h="400" class="right" %}}
{{% img src="/images/image.jpg" w="600" h="400" class="left" %}}
{{% img src="/images/image.jpg" w="600" h="400" caption="Referenced from wikipedia." href="https://en.wikipedia.org/wiki/Lorem_ipsum" %}}
```

## Twitter

```
{{% twitter tweetid="780599416621297xxx" %}}
```

# Development mode

Support development mode.

```
env HUGO_ENV="DEV" hugo server --watch --buildDrafts=true --buildFuture=true -t solit
```

This mode is

* Not show Google Analytics tags.
* Show `IsDraft`.
* Show `WordCount`.

And set `{{ if ne (getenv "HUGO_ENV") "DEV" }} Set elements here. {{ end }}` if you want to place only in a production environment.

## Development shell example.

```
#!/bin/bash

env HUGO_ENV="DEV" hugo server --watch --buildDrafts=true --buildFuture=true
```

# Inspired by

* [LinkedIn Redesign ~ Freebies Vol\.4 on Behance](https://www.behance.net/gallery/42205705/LinkedIn-Redesign-Freebies-Vol4)

# Using iconset

* [Iconset:watchify\-v1\-0\-80px icons \- Download 25 free & premium icons on Iconfinder](https://www.iconfinder.com/iconsets/watchify-v1-0-80px)

# Colorscheme

* [Material Design Colors, Material Colors, Color Palette \| Material UI](https://www.materialui.co/colors)

