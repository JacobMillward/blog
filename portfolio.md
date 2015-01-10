---
layout: page
title: Portfolio
---
##Featured

<table>
  {% for project in site.data.projects %}
  <tr>
    <td style="width: 150px">{{project.name}}</td>
    <td style="width:300px"><img src="{{site.baseurl}}{{project.image_url}}" style="width:300px;height:200px;" /></td>
    <td>
      <p>
        {{project.description}}
      </p>
      <p><a href="{{project.download_url}}">Download here &raquo;</a></p>
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
