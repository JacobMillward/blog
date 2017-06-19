---
layout: page
title: Portfolio
---
## Featured

<table>
  {% for project in site.data.projects %}
  <tr>
    <td style="width: 150px">{{project.name}}</td>
    <td style="width:300px"><a class="fancybox" rel="group" href="{{project.image_url}}"><img src="{{project.image_url}}" alt="" /></a></td>
    <td>
      <p>
        {{project.description}}
      </p>
      <p>
      {% if project.url %}
      <a href="{{project.url}}" target="_blank">View &raquo;</a>
      {% else %}
      <i>Oh no! This project is no longer online :(</i>
      {% endif %}
      </p>
    </td>
  </tr>
  {% endfor %}
  {% unless site.data.projects %}
  <tr>
    <td>Nothing here yet.</td>
  </tr>
  {% endunless %}
</table>

----

For other projects visit my [Github]({{site.github_url}}).
