---
layout: gallery
title: Progressive Web Apps
permalink: /pwa/
---

<div class="col-lg-8 offset-md-2">
  <div class="row">
    {% assign count = 0 %}
    {% for app in site.data.pwa.overview %}
      {% if count == 0 %}<div class="row">{% endif %}
      
      <div class="card p-3 m-2 text-center" style="width: 18rem;">
        <div class="card-title"><h4>{{ app.title }}</h4></div>
        <div class="row justify-content-center">
          <a href="{{ site.url }}{{ site.baseurl }}/pwa/{{ app.directory }}.html">
            <img class="img-thumbnail" alt="{{ app.title }}" src="{{ site.url }}{{ site.baseurl }}/assets/pwa/{{ app.thumbnail }}" style="width: 150px; height: 150px; object-fit: cover; border-radius: 20%;" />
          </a>
        </div>
      </div>
      
      {% if count == 1 %}</div>{% endif %}
      
      {% assign count = count | plus: 1 %}
      {% if count >= 2 %}
        {% assign count = 0 %}
      {% endif %}
    {% endfor %}

    {% if count != 1 and count != 0 %}
      </div>
    {% endif %}
  </div>
</div>