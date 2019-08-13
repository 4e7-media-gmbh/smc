---
layout: home
title: Hangout
---
<div class="bottom-content tags">
{% assign sorted = site.post | sort: 'date' | reverse %}
<div class="bottom-posts">
    {% for post in sorted  %}
    {% if post.tags contains "Hangout" %}
        <div class="post">
            <a href="{{post.url}}"><h2>{{post.title | capitalize}}</h2></a>
            <div class="bottom-header">
                <p>{{post.date | date_to_long_string }}</p>
                <p>{{ post.tags}}</p>
            </div>
            <a href="{{post.url}}"><img class="side-img" src="{{post.img}}"></a>
        </div>
    {% endif %}
    {% endfor %}
</div>

<div class="side-bar">
        <div class="fb-cont">
            <h3>FACEBOOK</h3>
            <a href="https://www.facebook.com/smClubAustria/"><img src="/img/fb.png"></a>
        </div>
        <div class="side-posts">
            <h3>MOST POPULAR ON SMCA</h3>
            {% for post in sorted %}
            {% if post.pop contains "pop" %}
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
    </div>
</div>