
![](https://www.gravatar.com/avatar/5f0a9777b6e3d0a462c6645dd1191b34?s=200)


{% for repository in site.github.public_repositories %}
  * {{ dump(repository) }}
{% endfor %}
