---
section: Create Content
nav_order: 3
title: Feature Includes
topics: Content; Bootstrap Components
gallery: true
---

Lesson Template contains a series of [Liquid "includes"](https://jekyllrb.com/docs/includes/) to simplify adding basic [Bootstrap 5 components](https://getbootstrap.com/docs/5.1/components/) to your Markdown content.
The includes can be found in the "_includes" folder of your project. 
Check the comments at the top of each include file for details about options and how to use them.

Examples below demonstrate the includes with sample include `code` followed by the rendered feature:

--------

## Figures 

- put any images you want to use in the "images" folder, or use a full URL to external images.
- in the markdown file where you want the image to appear, use the "figure.html" include on its own line, following the pattern: `{% raw %}{% include figure.html img="my-cat.jpg" alt="cat" caption="My cat" width="50%" %}{% endraw %}`
- figures will be centered, and can optionally be given a caption and percentage width.

Include code: 

`{% raw %}{% include figure.html img="uidaho-workshop.jpg" alt="workshop scene" caption="Library workshops!" width="75%" %}{% endraw %}`

Becomes:

{% include figure.html img="uidaho-workshop.jpg" alt="workshop scene" caption="Library workshops!" width="75%" %}

--------

## Gallery Figures 

- Same as Figure include, but adds a gallery viewer!
- All gallery figures on the page will be browseable in the gallery.
- Pages using this include **MUST** have `gallery: true` added to their front matter!

Include code: 

`{% raw %}{% include gallery-figure.html img="uidaho-workshop.jpg" alt="workshop scene" caption="Library workshops!" width="75%" %}{% endraw %}`

Becomes:

{% include gallery-figure.html img="uidaho-workshop.jpg" alt="workshop scene" caption="Library workshops!" width="75%" %}

----------

## Alerts

Include code:

`{% raw %}{% include alert.html text="This is a Bootstrap [Alert](https://getbootstrap.com/docs/5.1/components/alerts/)" align="center" color="success" %}{% endraw %}`

Becomes:

{% include alert.html text="This is a [Bootstrap Alert](https://getbootstrap.com/docs/5.1/components/alerts/)" align="center" color="success" %}

-----------

## Link Buttons 

Include code:

`{% raw %}{% include button.html text="Bootstrap Docs" link="https://getbootstrap.com/docs/5.1/components/buttons/" color="info" %}{% endraw %}`

Becomes:

{% include button.html text="Bootstrap Docs" link="https://getbootstrap.com/docs/5.1/components/buttons/" color="info" %}

---------

## Cards

Include code:

```{% raw %}
{% capture text %}
- Use a Liquid capture to create the text.
- Text can be formatted using markdown.
- Card image cap, header, and title are optional features.
- It magically becomes a [Bootstrap Card](https://getbootstrap.com/docs/5.1/components/card/).
{% endcapture %}
{% include card.html text=text header="Example Card" title="Title example" img="uidaho-workshop.jpg" %}{% endraw %}
```

Becomes: 

{% capture text %}
- Use a Liquid capture to create the text.
- Text can be formatted using markdown.
- Card image cap, header, and title are optional features.
- It magically becomes a [Bootstrap Card](https://getbootstrap.com/docs/5.1/components/card/).
{% endcapture %}
{% include card.html text=text header="Example Card" title="Title example" img="uidaho-workshop.jpg" %}

------------

## Accordion

Include code:

`{% raw %}{% include accordion.html title1="Example section" text1=example1 title2="Section two" text2=example2 title3="Section three" text3=example3 %}{% endraw %}`

Becomes:

{% include accordion.html title1="Section one" text1="Some text content" title2="Section two" text2="Some text content" title3="Section three" text3="Some text content" %}

------------

## Modal

Include code:

`{% raw %}{% include modal.html button="Try Me" color="success" title="Example Modal" text="This is a modal, with little text." %}{% endraw %}`

Becomes:

{% include modal.html button="Try Me" color="success" title="Example Modal" text="This is a modal, with little text." %}

-------------

## YouTube Embed

Include code:

`{% raw %}{% include video-embed.html video="https://youtu.be/moJgWrD6dwg" caption="Example caption" transcript="GitHub something..." %}{% endraw %}`

Becomes:

{% include video-embed.html video="https://youtu.be/moJgWrD6dwg" caption="Example caption" transcript="GitHub something..." %}

-------------

## Jumbotron

Include code:

`{% raw %}{% include jumbotron.html heading="Jumbotron Include" text="Paragraph content goes here." button-text="Learn more" button-color="outline-primary" button-link="https://github.com/evanwill/workshop-template-b" border=true %}{% endraw %}`

Becomes: 

{% include jumbotron.html heading="Jumbotron Include" text="Paragraph content goes here." button-text="Learn more" button-color="outline-primary" button-link="https://github.com/evanwill/workshop-template-b" border=true %}

-------------

## Question

Include code:

`{% raw %}{% include question.html header=Example Question" text="Question text goes here?" solution="The answer is hidden until user clicks." %}{% endraw %}`

Becomes:

{% include question.html header="Example Question" text="Question text goes here?" solution="The answer is hidden until user clicks." %}
