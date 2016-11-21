---
layout: index
---
{% for post in site.posts %}
<div>
  <a href="{{ post.url | prepend: site.baseurl | replace: '//', '/' }}" class="text-link">
    <h2>
        {{ post.title }}
    </h2>
  </a>
  <p class="post-meta">
      {{ post.date | date: "%B %-d, %Y" }}
  </p>
</div>
<hr>
{% endfor %}
