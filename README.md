## ResInsight System Documentation

[ResInsight System Documentation](https://magnesj.github.io/resinsight-system-doc)


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
