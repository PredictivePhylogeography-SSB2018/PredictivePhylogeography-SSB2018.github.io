---
layout: page
description: This page describes the whole project.
---

![cat]({{ site.baseurl }}/img/cat.png)
A working group at the [German Centre for Integrative Biodiversity Research](https://www.idiv.de/sdiv.html)

## Recent Posts

<!-- Posts -->
<ul id="posts">

	{% for post in site.posts %}

	  <li class="post">
	  	<h3><a href="{% if site.baseurl == "/" %}{{ post.url }}{% else %}{{ post.url | prepend: site.baseurl }}{% endif %}">{%if post.header %}{{ post.header }}{% else %}{{ post.title }}{% endif %}</a></h3>
      <time datetime="{{ post.date | date_to_xmlschema }}" class="by-line"> <i>{{ post.date | date_to_string }}</i> </time>
	  	<p>{{ post.content | strip_html | truncatewords:50 }}</p>
	  </li>

    {% endfor %}

</ul>
