---
layout: page
title: SECRET
subtitle: Statistical learning to decipher secretion systems in genomes
permalink: /
redirect_from:
  - /about/
  - /about.html
---

Predicting the function of a protein is one core challenge in biology. Protein
function is typically inferred using sequence comparison with proteins whose
function is known. This is problematic in many ways. In particular, proteins
can have very different sequences, and yet share the same function. Machine
learning approaches are thus more and more investigated to go beyond sequence
similarity when annotating protein functions in new organism.

This project is about investigating machine learning strategies to infer
whether a protein is involved in a secretion system.

![Secretion systems](../assets/img/projects/secretion_systems.png)


Secretion systems are complexes of proteins enabling a number of essential
functions for prokaryotic organisms (bacteria and archaea) such as acquiring
nutrients or invading host cells. There are currently 12 types of secretion
systems known, but we have very strong evidence to believe there are more
secretion systems types: annotating the entier set of genomes with those 12
types of secretion systems shows that some bacteria don't have any. Because of
the importance of secretion systems to interact with the environment and with
each other, as well as the difficulty of finding novel secretion systems (12
years of research in an experimental lab for the last type of secretion system
found), we believe that there are entire types of secretion systems yet to
discover.


## People

<div class="block">
{% for post in site.peoples %}
    {% include archive-people-index.html %}
{% endfor %}

<br />
  
</div>




## Publications

<div class="block">

{% for post in site.publications reversed %}
    {% include archive-single-cv.html %}
{% endfor %}
</div>

