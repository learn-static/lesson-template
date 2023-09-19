---
section_id: Create Content
nav_order: 3
title: Page Set Up
topics: Front Matter; Navigation
---

Content pages are written in markdown and can be enhanced using Liquid includes that are packaged with the template.
Start by editing the examples or creating new files in the "content" folder.

Each content page will be one file inside the "content" folder of your project.
The page *stubs* have the extension `.md` (meaning Markdown) and can be organized further into folders inside the "content" folder if desired.

## Front Matter

Each content page requires "YAML front matter" at the top of the file.
This information is used to configure the page and navigation added to the site's sidebar.

Use these values:

- `title:` (required) value will appear as the H1 header at the top of the page and in navigation links. 
- `nav:` use nav only if you would like a value different than the title to appear in the sidebar navigation (optional, this can be helpful if you want to use a shorter title in the nav).
- `topics:` will appear as a small feature below the title (optional). These can serve as keywords to help your readers understand the focus of the section.
- `description:` will appear as an indented text block below the title (optional). This gives you a chance to summarize the section contents. 
- `youtubeid:` will add an YouTube video embed (optional). Find the id in the YouTube link. For example, in `https://youtu.be/moJgWrD6dwg` or `https://www.youtube.com/watch?v=moJgWrD6dwg` the youtubeid is `moJgWrD6dwg`.
- Alternatively, if you don't want these features to appear on the page, you can over ride the layout by adding `layout:`  with the option `sidebar`, `page`, or `default`.

The sidebar navigation is set up using further front matter values following these rules:

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
