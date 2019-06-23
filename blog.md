---
layout: default
---
<div class="usa-grid">
    <div class="usa-width-one-whole usa-section">
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
    </div>
