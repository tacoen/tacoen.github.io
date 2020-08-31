
![](https://www.gravatar.com/avatar/5f0a9777b6e3d0a462c6645dd1191b34?s=200)

{% assign public_repositories =  %}
{% for repository in site.github.public_repositories limit: 9 %}
  * <a href='{{ repository.html_url }}'>{{ repository.name }}</a><br>{{ repository.description }}
    * {{ repository|json_encode(constant('JSON_PRETTY_PRINT')) }}
{% endfor %}
