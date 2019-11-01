---
layout: default
title: Blog
---
<h1>Latest Posts</h1>

<ul>
  {% for post in site.posts %}
    <li>
      <h2>
      <font size="3"> {{ post.date |date_to_string}} </font> 
      &emsp;
      <a href="{{ post.url }}" >
        
        {{ post.title }}
       
        </a>
      </h2>
      <p>{{ post.excerpt }}</p>
    </li>
  {% endfor %}
</ul>