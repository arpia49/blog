Once I started playing with <a href="https://www.home-assistant.io">Home Assistant</a> I really needed to write somewhere what was I doing so... here am I. Again :)
<ul>
  {% for post in site.posts %}
    <li>
      <a href="/blog{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>

May the force be with you!
