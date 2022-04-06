# workshop-template-s

**project not finished!**

Jekyll template for a simple workshop website with a sidebar using Bootstrap 5.

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
