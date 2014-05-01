---
layout: home
title: "Post Recenti"
tags: []
image:
  feature: typewriter.jpg
---


   <div id='bump'>
        <section class="article archive">
        <div class="overlay"></div>
        <div class="featured-image" style="background-image: url({{ site.url }}/images/typewriter.jpg)"></div>
          <article class="archive-wrap">
              <ol class="post-list">
                  {% for post in site.categories['ocma'] %}
                    {% if post.categories contains 'ocma' %}
                      <li>
                        <div class="deets" itemscope itemtype="http://schema.org/BlogPosting" itemprop="blogPost">
                            <h1><a href="{{ site.url }}{{ post.url }}">{{ post.title }}</a></h1>
                            <p class="date"><time datetime="{{ post.date | date_to_xmlschema }}" itemprop="datePublished">{{ post.author }} - {{ post.date | date: "%B %d, %Y" }}</time></p>
                            <p class="">{% if post.description %}{{ post.description  | strip_html | strip_newlines | truncate: 250 }}{% else %}{{ post.content | strip_html | strip_newlines | truncate: 250 }}{% endif %}</p>
                        </div>
                      </li>
                    {% endif %}
                  {% endfor %}
              </ol>
          </article>
        </section>
    </div>