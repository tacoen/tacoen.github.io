![tacoen-gravatar](https://www.gravatar.com/avatar/5f0a9777b6e3d0a462c6645dd1191b34?s=200)

How random is randomize?

## Repository
<div class='cards'>
{% assign public_repositories = site.github.public_repositories | sort: 'updated_at' | reverse %}
{% for repository in public_repositories limit:11 %}
{% if repository.name != 'tacoen.github.io' %}

<div>
### <a href='{{ repository.html_url }}'>{{ repository.name }}</a>
{{ repository.description }}
{% if repository.topics|length > 0 %}
<div class='topic-list'>{% for t in repository.topics %}<span class='topic'>{{ t }}</span> {% endfor %}</div>
{% endif %}
</div>

{% endif %}
{% endfor %}


<style type="text/css" rel="stylesheet">
 .cards { display: plex; }
 .cards > div { display: plex; }
.topic-list { display: block; font-size: .9rem; }
.topic { color: #fff; background: #999; display:inline-block; margin-right: .5rem; padding: .25rem .5rem; }
</style>
