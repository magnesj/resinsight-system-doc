## Welcome to GitHub Pages

You can use the [editor on GitHub](https://github.com/magnesj/resinsight-system-doc/edit/master/README.md) to maintain and preview the content for your website in Markdown files.

[test](test)

# items in docs folder
<ul>
  {% for post in site.docs %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>

# items in posts folder
<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>


# items in pages folder
<ul>
  {% for post in site.pages %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
      <a href="{{{ site.baseurl }}/{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>

# items in pages ise baseurl folder
<ul>
  {% for post in site.pages %}
    <li>
      <a href="{{ post.path | prepend:site.baseurl }}">{{ post.title }}</a>
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

[test](test)

