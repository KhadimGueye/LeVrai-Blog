---
layout: page
title : Le Vrai-Blog
category: blog
description: "Vous vivez quelque chose d’insolite ? Vous testez une aventure que peu de personnes ont vécue ? Vous voulez partager avec vos amis, votre famille ou le monde entier vos émotions ou compiler vos expériences dans un « journal de bord » ? Le LeVrai-Blog, fait pour ça !"
---

<div id="all-posts">
  {% for post in site.posts %}
    {%if post.tag != "book" %}
    {% if post.blog == true %}
      <div id="index-post-{% increment i %}" class="single-post">
        <div class="excerpt">
          <div class="date">{{ post.date | date: "%B %Y" }}</div>
          <div class="title">
            <a href="{{ BASE_PATH }}{{ post.url }}">
              {% if post.titlehtml %}
                {{ post.titlehtml }}
              {% else %}
                {{ post.title }}
              {% endif %}
            </a>
          </div>

          <p class="description">
            {{post.description}}
          </p>
        </div>
      </div>
    {% endif %}
    {% endif %}
  {% endfor %}
</div>
