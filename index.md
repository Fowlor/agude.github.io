---
layout: default
title: Home
description: >
  Hi there! I'm Alex Gude, a physicist and data scientist in Silicon Valley.
  This site is where you can find my thoughts on technology, data science,
  machine learning, and more!
---

{% assign twitter-name = site.author.twitter %}
{% assign github-name = site.author.github %}

# Hi there!

I'm **Alex Gude**, a data scientist with a passion for plots and algorithms,
but also cycling and photography. I got my start in the valley at [Insight
Data Science][insight]. In my previous life, I was a [high energy particle
physicist][hep] at CERN and a [cosmologist][scp] at Lawrence Berkeley Labs.

[insight]: https://www.insightdatascience.com
[hep]: http://www.hep.umn.edu/us-cms
[scp]: http://supernova.lbl.gov

I write about whatever catches my attention [here on this site][blog]; mostly
that means data science, machine learning, deep learning, and software
development related topics. My old work blog (with mostly deep learning stuff)
can be found at [Gab41][gab41]. If you're interested in my thoughts in real
time, follow me on Twitter: [@{{ twitter-name }}][twitter]

[blog]: /blog/
[gab41]: https://gab41.lab41.org/@Alex.Gude
[twitter]: https://twitter.com/{{ twitter-name }}

The code that I write lives on my [Github page][github]. Check it out! Bug
reports and pull requests welcome!

[github]: https://github.com/{{ github-name }}

## Recent Posts

Below you can find the most recent posts; older posts can be found on my
[blog][blog]:

{% for post in site.posts limit:5 %}
  {% comment %} Article cards with an image and description. {% endcomment %}
  {% include article_card.html
    url=post.url
    image=post.image
    image_alt=post.image_alt
    title=post.title
    description=post.description
  %}
{% endfor %}
