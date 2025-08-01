---
layout: page
icon: fas fa-stream
order: 1
permalink: /channels/
---

# Channels



## Tech Writing Channel

about everything I build.

[Visit Tech Writing Channel →](/channels/tech-writing/)

{% assign tech_posts = site.posts | where: 'categories', 'tech-writing' | sort: 'date' | reverse | limit: 3 %}
{% if tech_posts.size > 0 %}
**Recent Posts:**
{% for post in tech_posts %}
- [{{ post.title }}]({{ post.url | relative_url }}) - {{ post.date | date: '%B %d, %Y' }}
{% endfor %}
{% else %}
*No posts yet. Coming soon!*
{% endif %}

---

## Academic Learning Channel

about everything I learn.

[Visit Academic Learning Channel →](/channels/academic-learning/)

{% assign academic_posts = site.posts | where: 'categories', 'academic-learning' | sort: 'date' | reverse | limit: 3 %}
{% if academic_posts.size > 0 %}
**Recent Posts:**
{% for post in academic_posts %}
- [{{ post.title }}]({{ post.url | relative_url }}) - {{ post.date | date: '%B %d, %Y' }}
{% endfor %}
{% else %}
*No posts yet. Coming soon!*
{% endif %} 
