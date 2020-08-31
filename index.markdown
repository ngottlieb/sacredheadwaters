---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: page
title: "Table of Contents"
---

### What is Sacred Headwaters?

[Sacred Headwaters](https://sacredheadwaters.substack.com) is a bi-weekly newsletter that aims to guide a co-learning process about the existential issues and planetary limitations facing humanity and about how we can reorient civilization in a way that will enable us to thrive for centuries to come. Subscribe below if you haven't already:

<iframe src="https://sacredheadwaters.substack.com/embed" width="100%" height="150" frameborder="0" scrolling="no"></iframe>

## How to use this page

The newsletter is delivered bi-weekly via email using a platform called Substack, but it's grown to be such a broad collection of material that Substack's interface for browsing past issues doesn't allow readers to "catch up." This table of contents is meant to be both a reference and a guide. If you're just joining us, consider starting with issue #1 and then browsing as you see fit. Neither the English language nor the format of this page are conducive to communicating the complex nature of the relationships between these concepts, so don't feel confined by the order the issues were published in.

This table of contents lists the readings from each newsletter, but I'd highly recommend heading over to the newsletter itself (by clicking the title) where I've introduced each reading with context and a short summary.

## Table of contents

{% for issue in site.posts reversed %}

{::options parse_block_html="true" /}

<details>
  <summary markdown="span">
  **[{{issue.title}}]({{issue.source_url}}){:target="_blank"}**
  {{issue.description}}</summary>

- **Topics**: {{ issue.topics | join: ', ' }}
  {% for reading in issue.readings %}
- [{{reading.title}}]({{reading.url}}) {{reading.author}} ({{reading.time}})
  {% endfor %}
  {% if issue.book %}
- **Book recommendation**: [_{{issue.book.title}}_]({{issue.book.url}}), {{issue.book.author}}
{% endif %}
</details>

{% endfor %}
