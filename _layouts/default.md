<!DOCTYPE html>
<html lang="en">

  {% include head.md %}

  <body>
    <div class="container max-w-2xl mx-auto px-6 lg:px-0">
      
      {% include header.md %} 
      
      {{ content }}

      <ul>
        {% for post in site.posts %}
          <li>
            {% if post.external_url %}
            <a href="{{ post.external_url }}">{{ post.title }}</a>
            {{ post.date | date: "%m-%d-%Y"}}
            {% else %}
            <a href="{{ post.url }}">{{ post.title }}</a>
            {% endif %}
          </li>
        {% endfor %}
      </ul>

      {% include footer.md %}

          </div>
  </body>
</html>
