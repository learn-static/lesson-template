# lesson-template

Learn-Static Lesson Template is a minimal [Jekyll](https://jekyllrb.com/) project to create a simple lesson, workshop, or documentation website, with a [Bootstrap](https://getbootstrap.com/)-based theme, designed for hosting on [GitHub Pages](https://pages.github.com/).
It features a sidebar navigation providing clear structure for step by step content.
The sidebar nav supports pages nested into sections to help organize your lesson content. 

All content is written using basic Markdown, making it simple to write, edit, and reuse lesson materials.
The template provides Liquid includes to simplify adding Bootstrap components to your pages.
Writing content in this simple, reuseable format makes for a better [Open Educational Resource](https://en.wikipedia.org/wiki/Open_educational_resources) since anyone can make a copy and adapt.

Visit the [demo site](https://learn-static.github.io/lesson-template/) to view example output on GitHub Pages and basic documentation.
To use Lesson Template to create your own website --> make a copy and replace the template content with your own!

## How To Use Template

The [lesson-template repository](https://github.com/learn-static/lesson-template) is a template project --> to get started quickly, make a copy and replace the demo with your own content and customizations. 
The content pages serve as documentation and examples to copy from.

Overview: 

1. Click the green "Use this template" button on the [lesson-template repository](https://github.com/learn-static/lesson-template) to make your own new copy of the code (make sure you are logged into GitHub!).
2. Work on the GitHub web interface or clone to your local machine to edit files (tip: click `.` on any GitHub repository to [open the web editor](https://docs.github.com/en/codespaces/the-githubdev-web-based-editor)).
3. Edit the "_config.yml" file with your info (see [Basic Configuration](https://learn-static.github.io/lesson-template/content/start/configure.html)).
4. Edit/add the content pages in Markdown found in the "content" folder (see [Page Set Up](https://learn-static.github.io/lesson-template/content/docs/pages.html)).
5. Add any images to the "images" folder.
5. Commit on the web interface or push to GitHub from your local machine.
6. In your repository's settings, activate GitHub Pages, using main branch.

## Creating Content

Content follows these conventions:

- All documentation files are written in Markdown. For clearer version control, editing, accessibility, and reusability please:
    - write one sentence per line.
    - always provide a blank line between elements (i.e. headers, paragraphs, lists, code blocks are always followed by a blank line).
    - headers should follow logical order on page without skipping levels. The page template includes an "h1" using the `title` set in the front matter--thus additional headers on the page should start at "h2", i.e. `##` in markdown.
    - code and variables should be given `code` class using backticks, filenames should be given in "quotes".
- Markdown files are located in the "content" folder and can be further organized into folders inside if desired.

## Create Navigation 

The sidebar navigation menu is controlled by front matter added to each page. 
There are two ways a page can appear in the nav: individual or in a section drop down.

The nav follows these rules:

- **Individual listing:** To list a page in the nav individually, add `nav_order` to the front matter of a content page. e.g. `nav_order: 1`. Do *not* include `section_id` or `section` in the front matter.
- **Section dropdown:** To create a "section" drop down, on the first content page of the section, add `nav_order` and `section_id` to the front matter. The value of `section_id` will be displayed as the label for the section drop down. e.g. `section_id: Workshop Prep`. The page's title will be listed as the first item in the section dropdown.
- **Section pages:** To add additional pages to the section dropdown, add `section` and `nav_order` to the front matter of a markdown file. The value of `section` must match a `section_id` set up on another markdown file. The page's title will appear under the corresponding section dropdown. The pages in the section will sort according to `nav_order` within the section--however, the page that sets up the section (with `section_id`) will always be listed first. 

Note: 

- The nav listings (individual pages and sections) will be sorted by the value of `nav_order`.
- If a markdown stub does not have `nav_order` *or* `section` in the front matter, the page will **not** appear anywhere in the navigation. Occasionally you might want to create pages that aren't linked in the nav, just be sure to link to them from somewhere else!
- The values of `section_id` / `section` should be unique. If you create multiple sections with the same name, the nav won't work as expected!

### Example Front Matter

Individual listing:

```
---
nav_order: 1
title: Introduction
---
```

Section lead:

```
---
section_id: Getting Started
nav_order: 3
title: Install Git and GitHub Desktop
---
```

Section content:

```
---
section: Getting Started
nav_order: 2
title: Configure Git
---
```

## Template Assets 

This repository does not include a Gemfile because it is a very simple project. 
It was originally built using Ruby 2.5+ and Jekyll 3.7+; most recently used Ruby 3 and Jekyll 4.3.2.
It is designed to work with [GitHub Pages automatic build versions](https://pages.github.com/versions/).

The template makes use of a variety of open source libraries. 
These files are included in the 'assets/lib/" folder to ensure the project remains fully self contained.
These assets include:

- [Bootstrap](https://getbootstrap.com/)
- [Bootstrap Icons](https://icons.getbootstrap.com/)
- [flexsearch](github.com/nextapps-de/flexsearch) 
- [lazysizes](https://github.com/aFarkas/lazysizes)
- [spotlight gallery](https://github.com/nextapps-de/spotlight)

## License

Learn-Static documentation and general web content is licensed [Creative Commons Attribution-ShareAlike 4.0 International](http://creativecommons.org/licenses/by-sa/4.0/).
Learn-Static code is licensed [MIT](https://github.com/learn-static/lesson-template/blob/main/LICENSE). 
This license does not include external dependencies included in the "assets/lib" directory, which are covered by their individual licenses.
