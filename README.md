## ResInsight System Documentation

Published at [https://magnesj.github.io/resinsight-system-doc](https://magnesj.github.io/resinsight-system-doc)

Themes are located at [https://github.com/pages-themes](https://github.com/pages-themes)

[Introduction to layouts](https://learn.cloudcannon.com/jekyll/introduction-to-jekyll-layouts/)

# items in docs folder
<ul>
  {% for page in site.docs %}
    <li>
      <a href="{{ page.url | prepend:site.baseurl }}">{{ page.title }}</a>
    </li>
  {% endfor %}
</ul>

# items in posts folder
<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url | prepend:site.baseurl }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>

# items in pages using baseurl
<ul>
  {% for page in site.pages %}
    <li>
      <a href="{{ page.url | prepend:site.baseurl }}">{{ page.title }}</a>
    </li>
  {% endfor %}
</ul>

# items in docs collection
<ul>
  {% for post in docs %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>
