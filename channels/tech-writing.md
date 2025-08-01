---
layout: page
title: Tech Writing
permalink: /channels/tech-writing/
---

# Tech Writing

about everything I build.

## Featured Posts

{% assign tech_posts = site.posts | where: 'categories', 'tech-writing' | sort: 'date' | reverse | limit: 3 %}
{% if tech_posts.size > 0 %}
  {% for post in tech_posts %}
### [{{ post.title }}]({{ post.url | relative_url }})

**{{ post.date | date: '%B %d, %Y' }}**
{% if post.tags %} | Tags: {% for tag in post.tags limit: 3 %}`{{ tag }}`{% unless forloop.last %}, {% endunless %}{% endfor %}{% endif %}

{% if post.excerpt %}{{ post.excerpt }}{% endif %}

---
  {% endfor %}
{% else %}
*No featured posts yet. Coming soon!*
{% endif %}

## All Posts

{% assign all_tech_posts = site.posts | where: 'categories', 'tech-writing' | sort: 'date' | reverse %}
{% if all_tech_posts.size > 0 %}
  {% for post in all_tech_posts %}
### [{{ post.title }}]({{ post.url | relative_url }})

**{{ post.date | date: '%B %d, %Y' }}**
{% if post.tags %} | Tags: {% for tag in post.tags limit: 3 %}`{{ tag }}`{% unless forloop.last %}, {% endunless %}{% endfor %}{% endif %}

{% if post.excerpt %}{{ post.excerpt }}{% endif %}

---
  {% endfor %}
{% else %}
*No posts in this channel yet. Coming soon!*
{% endif %} 
