---
layout: page
—-—

We try to make code available for all our computational work.
 

By clicking on the paper title you can navigate to a complete run through of the available code, and links to the Github repository.

test new

<div class="content list">
    {% for post in site.posts %}
        {% if post.type contains 'about' %}
        <div class="list-item">
            <h3 class="list-post-title">
            <a href=“{{site.url}}{{post.url}}”>{{post.title}}</a></h3>
        </div>
        <p> {{post.content}} </p>
        {% endif %}
    {% endfor %}
</div>
	