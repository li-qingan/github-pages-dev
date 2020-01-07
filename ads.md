---
layout: default
title: Blog
---
<h1>Latest Recruitment</h1>

<ul>
{% for category in site.categories %}
  {% for ad in category[1] %}
    {% if category[0] == "job" %}
        <li>
        <h2>
        <font size="3"> {{ ad.date |date_to_string}} </font> 
        &emsp;
        <a href="{{ ad.url }}" >
            
            {{ ad.title }}
        
            </a>
        </h2>
        <p>{{ ad.excerpt }}</p>
        </li>
    {% endif %}
  {% endfor %}
{% endfor %}
</ul>