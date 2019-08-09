---
layout: home
---

{% assign sorted = site.post | sort: 'date' | reverse %}
<div class="side-posts">
    {% for post in sorted  %}
    {% if post.tags == "Tech" %}
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