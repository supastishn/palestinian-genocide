---
layout: post
title: Latest Post
permalink: /
---

{% assign reversed_posts = site.posts | reverse %}
{% assign first_post = reversed_posts[0] %}
{% assign second_earliest_post = site.posts[1] %}
<div class="home">
  {% if site.posts.size > 0 %}
    {{ first_post.content }}
  {% else %}
    <p>No posts yet. Check back soon!</p>
  {% endif %}

  {% if reversed_posts.size > 1 %}
    <div style="margin-top: 2em; text-align: center;">
      <a href="/amnesty-summary/terse-summary" class="button">Read the Summary &raquo;</a>
    </div>
  {% endif %}
</div>
