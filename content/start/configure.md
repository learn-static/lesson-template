---
section: Get Started
nav_order: 3
title: Basic Configuration
topics: _config.yml
---

Edit the "_config.yml" to get your workshop website set up with the basics such as `title`, `description` and `author`.
These are values that will populate the template elements of your website, such as header and footer.
Check comments (denoted by `#` in YAML) in the file for all the options!

Once you have edited the "_config.yml" to fill in your details, you are ready to start editing your [content pages]({{ '/content/docs/pages.html' | relative_url }}).

## Theme Customization [optional]

The "_config.yml" contains some variables that can customize the basic style of website. 
To use them, uncomment the line (i.e. delete the leading `#`) and fill in an appropriate value.

- `header-bg-color` - adds a background color to the top header, use a [css color value](https://www.w3schools.com/colors/colors_picker.asp), e.g. `"#ffebcd`
- `header-text-color` - changes the top header text color, which should be changed with the header background to ensure readability, e.g. `"#ffffff`
- `active-nav-color` - changes the color highlighting the current page in the sidebar nav, e.g. `#17916d`
- `text-color` - changes the body text color, e.g. `#111`
- `link-color` - changes the color used in hyperlinks, e.g. `#2c1fdd`
- `base-font-size` - changes the body text font size, use rem or px units, e.g. `1.1rem`

Note: to add your own custom CSS, use the file "_sass/_custom.scss".
Any CSS/SASS you add to this file will override the template and Bootstrap classes.

## URL Variables [optional]

If you are using GitHub Pages to host your site, these values should be left commented out. 
However, if you are manually building your site or hosting it else where, the `url` (the domain or subdomain such as "https://username.github.io") and `baseurl` (the path location such as "/workshop-example") values should be filled in.

## Robots Exclude [optional]

If you do **NOT** want Google to index your website, uncomment the line `noindex: true`.
