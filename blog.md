---
layout: default
---
<div class="grid-container">
    <h1>Blogs</h1>

    {% include blog-post.html blog_post_slug = sites.posts.content %} 


    <ul>
    {% for post in site.posts %}
        <li>
            <a href = "{{ post.url }}">{{ post.title }}</a> 
        </li>
    {% endfor %}

    </ul>
</div>
