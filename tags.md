---
layout: page
title: Tags
permalink: /tags/
---
<script language="javascript"> 
function toggle(id) {
    var ele = document.getElementById(id);
    var tag = document.getElementById(id + '-tag');
    if(ele.style.display == "block") {
          ele.style.display = "none";
          tag.style.filter = "invert(0%)";
    } else {
      ele.style.display = "block";
      tag.style.filter = "invert(100%)";
      window.location.hash = id;
    }
} 
</script>
<ul class="tag-cloud">
{% assign tags_semi_sorted = site.tags | sort -%}
{% assign tags_list = tags_semi_sorted | sort_natural -%}
{% if tags_list.first[0] == null -%}
{% for tag in tags_list -%}
<li id="{{ tag }}-tag" style="font-size: {{ tag | last | size | times: 100 | divided_by: tags_list.size | plus: 70 }}%">
<a href="javascript:toggle('{{ tag }}');">{{ tag }}</a>
</li>
{% endfor -%}
{% else -%}
{% for tag in tags_list -%}
<li id="{{ tag[0] }}-tag" style="font-size: {{ tag | last | size | times: 100 | divided_by: tags_list.size | plus: 70 }}%">
<a href="javascript:toggle('{{ tag[0] }}');">{{ tag[0] }}</a>
</li>
{% endfor -%}
{% endif -%}
<!-- {% assign tags_list = nil -%} -->
</ul>
{% for tag in tags_list -%}
<div id="{{ tag[0] }}" style="display: none">
<h2 class='tag-header' id="{{ tag[0] }}">{{ tag[0] }}</h2>
<ul>
{% assign pages_list = tag[1] -%}
{% for post in pages_list -%}
{% if post.title != null -%}
{% if group == null or group == post.group -%}
{% if page.url == post.url -%}
<li class="active">
<a href="{{ site.baseurl }}{{ post.url }}" class="active">{{ post.title }}</a>
</li>
{% else -%}
<li>
{% include post/link.html title = "" link = post.link -%}
{% include post/project.html title = "" project = post.project -%}
<a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a>
</li>
{% endif -%}
{% endif -%}
{% endif -%}
{% endfor -%}
{% assign pages_list = nil -%}
{% assign group = nil -%}
</ul>
</div>
{% endfor -%}