# My blog for little projects
Once I started playing with home assistant ( https://www.home-assistant.io ) I really needed to write somewhere what was I doing so... here am I. Again.

<ul>
  {% for post in site.posts %}
    <li>
      <a href="/blog{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>
