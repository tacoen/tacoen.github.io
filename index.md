![tacoen-gravatar](https://www.gravatar.com/avatar/5f0a9777b6e3d0a462c6645dd1191b34?s=200)

How random is randomize?

## Repository
{% assign public_repositories = site.github.public_repositories | sort: 'updated_at' | reverse %}
{% for repository in public_repositories limit:11 %}
{% if repository.name != 'tacoen.github.io' %}
### <a href='{{ repository.html_url }}'>{{ repository.name }}</a>
{{ repository.description }}
{% if repository.topics|length > 0 %}
<div class='topic-list'>{% for t in repository.topics %}<span class='topic'>{{ t }}</span> {% endfor %}</div>
{% endif %}


{% endif %}
{% endfor %}


<style type="text/css" rel="stylesheet">
.topic-list { display: block; font-size: .9rem; }
.topic { color: #fff; background: #999; display:inline-block; margin-right: .5rem; padding: .25rem .5rem; }
</style>
