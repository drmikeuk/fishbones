---
layout: page
title: "About"
nav: "yes"
sortTitle: "z"
---

Like cod, archaeological fish specialists are an endangered species and, to halt their population decline, the AHRC funded an initiative to develop a digital resource that would support the training and development of a new generation of fish specialists.

To achieve these aims, the country's main players in zooarchaeological research teamed up to run a series of training workshops for PhD students.

The workshops were held at the Universities of Bradford, Cambridge, Bournemouth and York, and were led by world-leading experts in fish analysis: Andrew Jones, James Barrett, Alison Locker, Shelia Hamilton-Dyer and Rebecca Nicholson. To capture and distil the expertise available at these events, all of the workshops were filmed and the resulting footage was cut together to produce a series of training e-lectures.

Alongside the workshops, the project created Fishbone, a digital reference collection. Whilst handling collections will always be the optimal resource for fish analysis, our online reference collection provides high-resolution digital images for key skeletal elements, taken at different views, for more than 90 species of Mediterranean and North Atlantic freshwater and marine fishes.

<div class="divider"><i class="fas fa-fish"></i></div>

Fish images on the list of [Common Names](/commonnames.html) and [Families](/families.html) were mostly sourced from _[The natural history of British fishes : including scientific and general descriptions of the most interesting species, and an extensive selection of accurately finished coloured plates, taken entirely from original drawings, purposely made from the specimens in a recent state, and for the most part whilst living](https://www.nypl.org/research/research-catalog/bib/b11399861?originalUrl=https%3A%2F%2Fcatalog.nypl.org%2Frecord%3Db11399861)_ and _[Ichtylogie, ou Histoire naturelle : génerale et particuliére des poissons](https://www.nypl.org/research/research-catalog/bib/b13637086?originalUrl=https%3A%2F%2Fcatalog.nypl.org%2Frecord%3Db13637086)_ from the New York Public Library. Links to each source are listed below:

{% assign fishes = site.data.fish | sort: "Name" %}
{% for fish in fishes %}<a href="{{ fish.sourceurl }}">{{ fish.Name }}</a>{% if forloop.last %}{% else %}, {% endif %}{% endfor %}.

Icons are from <a href="https://fontawesome.com/">Font Awesome</a> and <a href="https://www.freepik.com" title="Freepik">Freepik</a>.

Except for third party materials (materials owned by someone other than The University of Nottingham) and where otherwise indicated, the copyright in the content provided on this site is owned by The University of Nottingham and licensed under a <a href="https://creativecommons.org/licenses/by-nc-sa/2.0/uk/">Creative Commons Attribution-NonCommercial-ShareAlike UK 2.0 Licence (BY-NC-SA)</a>.
