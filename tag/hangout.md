---
layout: tagpage
title: "tags: hangout"
tags: Hangout
---
<div class="side-posts">
            <h3>MOST POPULAR ON SMCA</h3>
            {% for post in sorted %}
            {% if post.tags== 1 %}
            <div class="side-post">
                <a href="{{post.url}}"><div class="side-img" style="background-image:url('{{post.img}}')"></div></a>
                <a href="{{post.url}}"><h2>{{post.title | capitalize}}</h2></a>
                <div class="side-header">
                    <p>{{post.date | date_to_long_string }}</p>
                    <p>{{ post.tags}}</p>
                </div>
            </div>
            {% endif %}
            {% endfor %}
        </div>