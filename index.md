
![](https://www.gravatar.com/avatar/5f0a9777b6e3d0a462c6645dd1191b34?s=200)

{% assign public_repositories = site.github.public_repositories | sort: 'updated_at' | reverse %}

{% for repository in public_repositories limit:5 %}

{% if repository.name != 'tacoen.github.io' %}
  * <a href='{{ repository.html_url }}'>{{ repository.name }}</a><br>{{ repository.description }}
    * {{ repository|json_encode(constant('JSON_PRETTY_PRINT')) }}
{% endif %}

{% endfor %}
