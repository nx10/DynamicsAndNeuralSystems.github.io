---
title: "Dynamics and Neural Systems Group - Publications"
layout: gridlay
excerpt: "Dynamics and Neural Systems Group -- Publications."
sitemap: false
permalink: /publications/
---

# Publications

Here we list some key research publications from the Dynamics and Neural Systems Group.

For BD Fulcher's full publication list, see [Google Scholar](https://scholar.google.com.au/citations?user=iQYJOW4AAAAJ).

## Recent Highlights

{% assign number_printed = 0 %}
{% for publi in site.data.publist %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if publi.highlight == 1 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
 <div class="well">
  <pubtit>{{ publi.title }}</pubtit>
  <img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ publi.image }}" class="img-responsive" width="33%" style="float: left" />
  <p>{{ publi.description }}</p>
  <p>{{ publi.authors }}</p>
  <p><a href="{{ publi.link.url }}"><em>{{ publi.link.journal }}</em> ({{publi.link.year}}).</a></p>
  <p class="text-danger"><strong> {{ publi.news1 }}</strong></p>
  <p> {{ publi.news2 }}</p>
 </div>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endif %}
{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

<p> &nbsp; </p>


## More from our group

{% for publi in site.data.publist %}

  {{ publi.title }}.<br />
  {{ publi.authors }}.
  <a href="{{ publi.link.url }}"><em>{{ publi.link.journal }}</em> ({{publi.link.year}}).</a>

{% endfor %}
