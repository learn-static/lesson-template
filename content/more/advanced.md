---
section: Customize
nav_order: 2
title: Advanced Customization Options
topics: CSS
---

The Lesson Template theme is build using [Bootstrap 5](https://getbootstrap.com/). 
Once you understand how it works, you can dig into the template code and make your own tweaks!

## Add Custom CSS

The best way to add custom CSS rules to your site is by editing the "_sass/_custom.scss" file. 
CSS or [SASS](https://sass-lang.com/) that you place in this file will override Bootstrap and the template's classes. 

The template's SASS is contained in "_sass/template.scss".
These rules style the sidebar and content features.
Rather than editing directly, it is better to override them using "_custom.scss".

The "SASS partials" contained in the "_sass" folder are pulled into the final CSS file "assets/css/main.scss".
In general "main.scss" does not need to be edited.

## Tweak Includes 

Modular chucks of the template's theme can be found in "_includes/template/" folder.
These includes create component parts such as the header or javascript included on every page.

You might be interested in editing the content of a few:

- "credits.html" -- attempts to auto generates creates for the front page of your site based on config values.
- "sidebar-footer.html" -- controls the information at the bottom of the sidebar nav.
- "analytics.html" - To add analytics to your project, paste the tracking snippet provided by your platform (such as Matomo or Google Analytics) into this file. The analytics code will only be added when using "production" environment, so that you will avoid triggering hits during development. The "production" environment is used automatically on GitHub Pages. To build manually on your local machine you will need to add "JEKYLL_ENV", like: `JEKYLL_ENV=production jekyll build`.

You can also always add additional includes to the folder if you have a template feature that you want to use in your content!

## Edit Layouts

The templates that control the final layout of all pages are in the "_layouts" folder.

All pages in the "content" folder default to the "lesson-content.html" layout. 
If you would like your page to follow a different layout, manually set the layout in the front matter: `layout: example`.

All pages eventually use the "default.html" which contains the header and sidebar nav.
