```twig
<h1>{{ title }}</h1>
<ul>
    {% for id, post in posts %}
        <li><a href="/blog/{{ id }}">{{ post }}</a></li>
    {% endfor %}
</ul>
```

![Rendered twig template screenshot](resources/twig-rendered.png)
