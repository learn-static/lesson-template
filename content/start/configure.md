---
section: Get Started
nav_order: 3
title: Basic Configuration
topics: Site options; _config.yml
---

In your project repository, edit the "_config.yml" file to get your workshop website set up with the basics such as `title`, `description` and `author`.
Check comments (denoted by `#` in YAML) in the file for all the options!

Once you have edited the "_config.yml" to fill in your details, you are ready to start editing your [content pages]({{ '/content/docs/pages.html' | relative_url }}).

## Site Settings

The values in this section of "_config.yml" will populate the template elements of your website, such as header and footer.
Replace the template values with your own details.

At minimum, be sure to fill in `title`.
The other values are optional, but strongly suggested.

The `publication_year`, `source-code` link, `content_license`, and `content_license_link` are displayed at the bottom of the sidebar nav and in the credits section of the home page. 
Filling these options in ensures others can properly reuse and cite your content.

## Theme Customization [optional]

The "_config.yml" contains some variables that can customize the basic style of website.
These options are added to the template CSS, so the values must be valid in CSS (i.e. an [html color value](https://www.w3schools.com/colors/colors_picker.asp), usually hash is easiest such as `#66ff33`).
Please take care with your custom selections to ensure there is enough contrast between the background and text colors for accessibility.

To use the options, uncomment the line (i.e. delete the leading `#`) and fill in an appropriate value.
If you are using a hash color value, you will need to put quotes around it.

- `header-background` - adds a background color to the top header, e.g. `"#ffebcd"`
- `header-text-color` - changes the top header text color, which should be changed with the header background to ensure readability, e.g. `"#ffffff"`
- `breadcrumbs-background` - changes the background color of the breadcrumbs bar, e.g. `"#ffebcd"`
- `breadcrumbs-text-color` - changes the breadcrumbs bar text color, which should be changed with the breadcrumbs background to ensure readability, e.g. `"#ffffff"`
- `active-nav-color` - changes the color highlighting the current page in the sidebar nav, keep in mind that nav text is black, so this should be a light color to ensure contrast, e.g. `"#17916d"`
- `link-color` - changes the color used in hyperlinks, e.g. `"#2c1fdd"`
- `next-button-color` - changes the border color of the prev / next buttons at the bottom of content pages, e.g. `"#2c1fdd"`
- `text-color` - changes the body text color, e.g. `"#111"`
- `base-font-size` - changes the body text font size, use rem or px units, e.g. `1.1rem`

Note: to add your own custom CSS, use the file "_sass/_custom.scss".
Any CSS/SASS you add to this file will override the template and Bootstrap classes.

## URL Variables [optional]

If you are using GitHub Pages to host your site, these values should be left commented out.

However, if you are manually building your site or hosting it else where, the `url` (the domain or subdomain such as "https://username.github.io") and `baseurl` (the path location such as "/workshop-example") values should be filled in.
Neither value should have a trailing `/` slash.

## Robots Exclude [optional]

If you do **NOT** want Google to index your website, uncomment the line `noindex: true`.
