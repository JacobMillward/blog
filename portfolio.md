---
layout: page
title: Portfolio
---

##### For other projects visit my [Github]({{site.github_url}}).
----
{% for project in site.data.projects %}
  <h3>{{project.name}}</h3>
  <section class="splitContainer">
    <div class="leftSide">
    {% if project.image_url %}
      <a class="fancybox" rel="group" href="{{project.image_url}}"><img src="{{project.image_url}}" alt="" /></a>
      <i>Click to expand</i>
    {% else %}
      <p><i>Sorry, no image :(</i></p>
    {% endif %}
    </div>
    <div class="rightSide">
      <p>
        {{project.description}}
      </p>
        {% if project.url %}
        <p>
          <a href="{{project.url}}">View &raquo;</a>
        </p>
        {% endif %}
        {% if project.demo %}
        <p>
          <a href="{{project.demo}}">Demo &raquo;</a>
        </p>
        {% endif %}
    </div>
  </section>
  <hr />
{% endfor %}
{% unless site.data.projects %}
## Nothing here yet. :(
{% endunless %}
