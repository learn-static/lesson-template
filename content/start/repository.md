---
section: Get Started
nav_order: 2
title: Create Project
topics: Template; Basic Config
---

The [lesson-template repository](https://github.com/learn-static/lesson-template) is a template project --> to get started quickly, make a copy and replace the demo with your own content and customizations.

The [demo site](https://learn-static.github.io/lesson-template/) demonstrates the output on GitHub Pages.
The content pages in the repository serve as documentation and examples to copy from.

{% capture text %}
1. Click the green "Use this template" button on the [lesson-template repository](https://github.com/learn-static/lesson-template) to make your own new copy of the code (make sure you are logged into GitHub!).
2. Work on the GitHub web interface or clone to your local machine to edit files (tip: click `.` on any GitHub repository to [open the web editor](https://docs.github.com/en/codespaces/the-githubdev-web-based-editor)).
3. Edit the "_config.yml" file with your info.
4. Edit/add the content pages in Markdown (found in the "content" folder).
5. Add any images to the "images" folder.
5. Commit on the web interface or push to GitHub from your local machine.
6. In your repository's settings, activate GitHub Pages, using main branch.
{% endcapture %}
{% include card.html header="Create Repository" text=text %}
