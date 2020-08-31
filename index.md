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
.cards {display: flex;justify-content: space-evenly;flex-direction: row;flex-wrap: wrap;}
.cards > div {display: block;padding:  .5rem;border: 1px solid #0003;border-radius: .25rem;margin: 0 1rem 1rem 0;}
.topic-list { display: block; font-size: .9rem; }
.topic { color: #fff; background: #999; display:inline-block; margin-right: .5rem; padding: .25rem .5rem;border-radius: .15rem }
<</style>
