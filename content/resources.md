---
nav_order: 5
title: Reference & Resources
---

To learn about using Lesson Template, the content pages of this demo provide documentation and examples (also check the [README](https://github.com/learn-static/lesson-template/blob/main/README.md)).

Workshop sites using this template:

- [Demo](https://learn-static.github.io/lesson-template/) (this repository) 

# Reference

## Git & GitHub

[GitHub](https://github.com/) is a popular web service for hosting Git repositories--with benefits!
It provides a handy web interface for editing and collaborating on repos, as well as, built in project management features and [free static web hosting](https://pages.github.com/) powered by [Jekyll](https://jekyllrb.com/).
Accounts are free.
To learn more check out Hello World on [GitHub Guides](https://guides.github.com/) or [GitHub Learning Lab](https://lab.github.com/).

## Markdown

[Markdown](https://daringfireball.net/projects/markdown/) is a standard to simplify writing content for the web. 
Markdown can be used any where on GitHub and in Jekyll.

- [Mastering Markdown GitHub Guide](https://guides.github.com/features/mastering-markdown/){:target="_blank" rel="noopener"}
- [GitHub Markdown documentation](https://docs.github.com/en/free-pro-team@latest/github/writing-on-github/basic-writing-and-formatting-syntax){:target="_blank" rel="noopener"}
- [Markdown in a Minute](https://evanwill.github.io/_drafts/notes/markdown-minute.html)

## Bootstrap 5

[Bootstrap](https://getbootstrap.com/) is a CSS framework designed to streamline developing user interfaces for your website.

[Bootstrap Icons](https://icons.getbootstrap.com/) are SVG-based icon set used to add graphics to your content.

## YAML

[YAML](http://www.yaml.org/) is a human readable plain text data format.
It is used in Jekyll for configuration, site data, and front matter.
Jekyll projects are [configured](https://jekyllrb.com/docs/configuration/) using the "_config.yml" file.

## Liquid

[Liquid](http://shopify.github.io/liquid/) is a flexible template language.
[In Jekyll]((https://jekyllrb.com/docs/liquid/) it allows you to layout pages built from modular components and data, using the "_includes", "_layouts", and "_data" directories.
Liquid includes features such as operators, loops, and filters to manipulate raw content. 
Liquid statements are enclosed by {% raw %}`{%  %}`{% endraw %} and variables in {% raw %}`{{  }}`{% endraw %}.

## Sass  

[Sass](http://sass-lang.com/) is a CSS extension / preprocessor. 
All normal CSS is valid SCSS, but Sass adds many powerful functions and programmatic features. 
Writing SCSS is often easier and more sensible, for example by supporting nesting, variables, and operators. 
Jekyll lets you write SASS in modular chucks called partials, in the "_sass" directory, that will be combined and compiled into normal CSS files when the site is built.
