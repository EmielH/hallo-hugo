# Hallo

[![Build Status](https://travis-ci.com/EmielH/hallo-hugo.svg?branch=master)](https://travis-ci.com/EmielH/hallo-hugo)

Hallo is a single-page Hugo theme for personal introductions. Add a portrait, an introduction, several links, and you're set.

![Hallo screenshot](https://raw.githubusercontent.com/EmielH/hallo-hugo/master/images/screenshot.png)

## Installation

### 1. Install the theme

If your site is also under version control using git, the easiest way to install this theme is to add it as a submodule. If you have not created a git repo for your project yet, you need to run `git init` beforehand. Inside the folder of your Hugo site, run the following command.

```
git submodule add https://github.com/EmielH/hallo-hugo.git themes/hallo
```

Alternatively, you can clone the theme into your project.

```
git clone https://github.com/EmielH/hallo-hugo.git themes/hallo
```

### 2. Configure Hugo

Add the following line to `config.toml` to tell Hugo to use the theme.

```
theme = "hallo"
```

Alternatively, you can tell Hugo to use the theme with the `server` command.

```
hugo server -t hallo
```

_[Hugo setup guide](https//gohugo.io/overview/installing/)_

### Update the theme

If you have installed the theme as a git submodule, you can update the theme by issuing the following command inside your project folder.

```
git submodule update --remote --rebase
```

If you have cloned the theme, you can run `git pull` inside the theme folder.

## Configuration

### Portrait

Put your own portrait in `/static/images/portrait.jpg` of your own site and Hugo wil automatically use that portraid instead of the standard one. It's not necessary to alter the theme.

### Introduction

Put your own introduction text in `/layouts/partials/introduction.html` of your own site and Hugo wil automatically use that introduction instead of the standard one. It's not necessary to alter the theme.

### Name

Hallo will use the name of the author that has been configured in the `Author` section of your site's `config.toml`. Add the lines below to your `config.toml` to configure the name.

```
[Author]
    name = "Emiel"
```

### Links

You can put your own links below the introduction text, for example to link to your social media accounts or to include your e-mail address. These links use icons from FontAwesome. The links can be configured in the `params` section of your site's `config.toml`. This is an example configuration for a link to Github:

```
[params]
    [[params.links]]
        icon = "github"
        title = "Github"
        url = "https://github.com/"
```

Hallo by default allows you to choose an icon from [the brands set](https://fontawesome.com/icons?d=gallery&s=brands&m=free). Put the name of the icon in the `icon` parameter. This set is the default set because these links will mostly be used for links to social media.

It is possible to use an icon from [the solid set](https://fontawesome.com/icons?d=gallery&s=solid&m=free). To do this, specify the icon set, like this:

```
    [[params.links]]
        iconset = "fas"
        icon = "envelope"
        title = "E-mail"
        url = "mailto:mail@example.org"
```

### Internationalisation (i18n)

Hallo supports using other languages than English. Language files for the texts Hallo uses are provided in the `i18n` directory. The default language is English. To switch languages, add the key `defaultContentLanguage` to your `config.toml` file. For example:

```
defaultContentLanguage = "nl"
```

To translate texts your site uses, add an `i18n` folder to your site.

Feel free to submit pull requests for other translations of Hallo's texts.

_[Hugo documentation for multilingual sites](//gohugo.io/content-management/multilingual/)_

### Colours

You can alter the colours of your website using configuration options. Add the following to the `[params]` section of your `config.toml` for an alternate colour scheme:

```
    [params.colors]
        background = "#81c6ff"
        foreground = "#edf7ff"
        hover = "#ffba82"
```

* `background`: Used as background colour of the site.
* `foreground`: Used for text and the border of the portrait.
* `hover`: Used for hover of links.

## Acknowledgments

Stock portrait photo obtained [here](https://www.pexels.com/photo/adult-beautiful-blonde-blur-324658/).

## License
See [LICENSE](https://github.com/EmielH/hallo-hugo/blob/master/LICENSE).
