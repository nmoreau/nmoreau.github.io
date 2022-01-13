# Blog-ish Random notes and thoughts

This is the place where I will host some good reads, ideas, notes, and samples.

{% include badges.md %}


<!-- Index of Posts -->

   {% for post in site.posts %}
    <article>
        <h2>
        <a href="{{ post.url }}">
            {{ post.title }}
        </a>
        </h2>
        {{ post.excerpt }}
        <br/>
        posted on <time datetime="{{ post.date | date: "%Y-%m-%d" }}">{{ post.date | date_to_long_string }}</time>
        <br/>
        <br/>
    </article>
  {% endfor %}

<!-- End index of Posts -->
