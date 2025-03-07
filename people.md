# People

````{jinja} people

{% for category, cat_people in people.items() %}

## {{ category | replace("_", " ") }}

{% for person in cat_people %}

### {{ person.name }}

{% if person.pic %}
```{image} _static/images/{{ person.pic }}
:width: 200px
:class: biopic
:alt: {{ person.name }}
```
{% endif %}

{% if person.email %}
[{{ person.email }}](mailto:{{ person.email }})
{% endif %}

{% if person.pronouns %}
```{image} https://img.shields.io/static/v1?label=pronouns&message={{ person.pronouns }}&color=red&style=flat-square
   :alt: Pronouns
```
{% endif %}

{% if person.orcid %}
```{image} https://img.shields.io/static/v1?label=ORCID&message={{ person.orcid }}&color=green&style=flat-square&logo=orcid
   :alt: ORCID Profile
   :target: https://orcid.org/{{ person.orcid }}
```
{% endif %}

{% if person.scholar %}
```{image} https://img.shields.io/static/v1?label=&message=Google%20Scholar&color=gray&style=flat-square&logo=google-scholar
   :alt: Google Scholar
   :target: https://scholar.google.com/citations?user={{ person.scholar }}
```
{% endif %}

{% if person.researchgate %}
```{image} https://img.shields.io/static/v1?label=&message=ResearchGate&color=gray&style=flat-square&logo=ResearchGate
   :alt: ResearchGate
   :target: https://www.researchgate.net/profile/{{ person.researchgate }}
```
{% endif %}

{% if person.github %}
```{image} https://img.shields.io/github/followers/{{ person.github }}?label=Github&logo=github&style=flat-square
   :alt: GitHub Profile
   :target: http://github.com/{{ person.github }}
```
{% endif %}

{% if person.twitter %}
```{image} https://img.shields.io/twitter/follow/{{ person.twitter }}?logo=twitter&style=flat-square
    :alt: Twitter
    :target: https://twitter.com/{{ person.twitter }}
```
{% endif %}

{% if person.linkedin %}
```{image} https://img.shields.io/static/v1?label=&message=LinkedIn&color=0077B5&style=flat-square&logo=linkedin
   :alt: Google Scholar
   :target: https://www.linkedin.com/in/{{ person.linkedin }}
```
{% endif %}

{% if person.website %}
```{image} https://img.shields.io/website?style=flat-square&url={{ person.website|urlencode }}
    :alt: Website
    :target: {{ person.website }}
```
{% endif %}


{{ person.bio }}


{% endfor %}
{% endfor %}

````

## Alumni

````{jinja} alumni

{% for person in alumni %}

### {{ person.name }}

{% if person.pic %}
```{image} _static/images/{{ person.pic }}
:width: 200px
:class: biopic
:alt: {{ person.name }}
```
{% endif %}

{% if person.pronouns %}
```{image} https://img.shields.io/static/v1?label=pronouns&message={{ person.pronouns }}&color=red&style=flat-square
   :alt: Pronouns
```
{% endif %}

{% if person.orcid %}
```{image} https://img.shields.io/static/v1?label=ORCID&message={{ person.orcid }}&color=green&style=flat-square&logo=orcid
   :alt: ORCID Profile
   :target: https://orcid.org/{{ person.orcid }}
```
{% endif %}

{% if person.scholar %}
```{image} https://img.shields.io/static/v1?label=&message=Google%20Scholar&color=gray&style=flat-square&logo=google-scholar
   :alt: Google Scholar
   :target: https://scholar.google.com/citations?user={{ person.scholar }}
```
{% endif %}

{% if person.researchgate %}
```{image} https://img.shields.io/static/v1?label=&message=ResearchGate&color=gray&style=flat-square&logo=ResearchGate
   :alt: ResearchGate
   :target: https://www.researchgate.net/profile/{{ person.researchgate }}
```
{% endif %}

{% if person.github %}
```{image} https://img.shields.io/github/followers/{{ person.github }}?label=Github&logo=github&style=flat-square
   :alt: GitHub Profile
   :target: http://github.com/{{ person.github }}
```
{% endif %}

{% if person.twitter %}
```{image} https://img.shields.io/twitter/follow/{{ person.twitter }}?logo=twitter&style=flat-square
    :alt: Twitter
    :target: https://twitter.com/{{ person.twitter }}
```
{% endif %}

{% if person.linkedin %}
```{image} https://img.shields.io/static/v1?label=&message=LinkedIn&color=0077B5&style=flat-square&logo=linkedin
   :alt: Google Scholar
   :target: https://www.linkedin.com/in/{{ person.linkedin }}
```
{% endif %}

{% if person.website %}
```{image} https://img.shields.io/website?style=flat-square&url={{ person.website|urlencode }}
    :alt: Website
    :target: {{ person.website }}
```
{% endif %}

_**{{ person.position }}**_

Current position: {{ person.current_position}}

{% if person.other_positions %}
Past positions: {% for item in person.other_positions %} {{ item  }}, {% endfor %}
{% endif %}



{% endfor %}

````
