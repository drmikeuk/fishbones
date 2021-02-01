---
layout: home
title: "Videos"
nav: "yes"
sortTitle: "g"
---

<!-- HEADER -->
<div class="home">
	<div class="container">
	</div>
</div>

<!-- TILES -->
<div class="container">

	<h2>Videos</h2>

	<p>Workshops held at the Universities of Bradford, Cambridge, Bournemouth and York by world-leading experts in fish analysis. All workshops were filmed and the resulting footage used to produce this series of training e-lectures.</p>

	<div class="row tiles">
	{% for video in site.data.videos %}
		{% include videotile.html %}
	{% endfor %}
	</div>


</div>
