---
layout: page
title: Notes
permalink: /notes/
---
<div class="notes">
{% for note in site.notes %}
  <article class="note">    
  <h1>{% 
    <a href="{{ site.baseurl }}{{ note.url }}">{{ note.title }}</a></h1> 
  {% include post/meta.html %}
    <div class="entry">
      {{ note.excerpt }}
    </div>
  </article>
{% endfor %}
</div>