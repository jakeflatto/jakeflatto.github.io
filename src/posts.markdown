---
title:  "Blog, i guess"
---
<div>
  <a href="/">Home</a> > <a href="#0">Blog, i guess</a>
</div>
What's a personal website without a Blog, i guess? 

No idea how often I will actually intend to post here. 
But one thing I like about the idea of having a blog on my page is: 
it allows me to broadcast ideas without the use of traditional social media.

And you certainly won't find any references to traditional social media anywhere on my site.
Definitely not at the bottom of this or any other page.

**Posts**
{% if site.posts.size == 0 %}
<div class="img-container">
  <img src="/assets/images/footage_not_found.png" alt="Footage not found">
</div>
{% else %}
<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>
{% endif %}
