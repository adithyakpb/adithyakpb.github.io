---
layout: page
title: Academic Learning
permalink: /channels/academic-learning/
---

# Academic Learning

about everything I learn.

## Featured Posts

{% assign academic_posts = site.posts | where: 'categories', 'academic-learning' | sort: 'date' | reverse | limit: 3 %}
{% if academic_posts.size > 0 %}
  {% for post in academic_posts %}
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

{% assign all_academic_posts = site.posts | where: 'categories', 'academic-learning' | sort: 'date' | reverse %}
{% if all_academic_posts.size > 0 %}
  {% for post in all_academic_posts %}
### [{{ post.title }}]({{ post.url | relative_url }})

**{{ post.date | date: '%B %d, %Y' }}**
{% if post.tags %} | Tags: {% for tag in post.tags limit: 3 %}`{{ tag }}`{% unless forloop.last %}, {% endunless %}{% endfor %}{% endif %}

{% if post.excerpt %}{{ post.excerpt }}{% endif %}

---
  {% endfor %}
{% else %}
*No posts in this channel yet. Coming soon!*
{% endif %} 
