---
layout: default
title: works
permalink: /works/
---

<div class="row" id="intro">
  <h1>{{ page.title }}</h1>
</div>


{% for post in site.posts %}

 {% if post.categories contains 'video' %}
  <div class="small-12 large-4 medium-5 columns">
    <a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
    <p>{{ post.date | date: "%b %-d, %Y" }}</p>
    <div class="videoWrapper">
      <iframe src="https://player.vimeo.com/video/{{ post.videourl }}?title=0&byline=0&portrait=0" width="100%" height="400" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>
    </div>
  </div>
 {% endif %} 

 {% if post.categories contains 'sound' %}	
  <div class="small-12 large-4 medium-5 columns">
   <a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
   <p>{{ post.date | date: "%b %-d, %Y" }}</p>
   <iframe width="100%" height="166" scrolling="no" frameborder="no" src="https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/{{post.sound}}&amp;color=ff5500&amp;auto_play=false&amp;hide_related=false&amp;show_comments=true&amp;show_user=true&amp;show_reposts=false"></iframe>
  </div>
 {% endif %}

{% endfor %}