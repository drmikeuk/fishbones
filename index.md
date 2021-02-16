---
layout: home
title: "Elements"
nav: "yes"
sortTitle: "bb"
filter: "yes"
---

<!-- HEADER -->
<div class="home">
	<div class="container">
		<div class="title">
			<h1>{{ site.title }}</h1>
		</div>
	</div>
</div>

<!-- TILES -->
<div class="container">

	<p class="strap">{{ site.blurb }}</p>


	<div class="row title">
		<div class="col">
			<h2>Browse by element</h2>
		</div>
		<div class="col-lg-3 col-md-3 col-sm-12">
		<form class="form-inline">
			 <input class="form-control" id="filterFish" type="text" placeholder="Filter...">
		</form>
		</div>
	</div>


	<div class="row tiles">
	<!-- 'map' so only category property + 'uniq' to remove duplicates => simple list of cats -->
	{% assign Elements = site.data.fishbones | map: "Element"| uniq | sort  %}
	{% for Element in Elements %}
	<div class="col-lg-3 col-md-6 col-sm-12 pb-4">
	  {% assign thumb = Element | remove: " " | remove: "(" | remove: ")" | downcase | prepend: "/elementThumbs/"| append: ".jpg" %}
	  {% assign link = Element | remove: " " | remove: "(" | remove: ")" | downcase | prepend: "/Element/"| append: ".html" %}
	  <div class="tile">
	    <a href="{{ link }}">
	      <div class="tile" style="background-image: url({{thumb}})">
	        <p>{{ Element | capitalize }} <i class="fas fa-chevron-circle-right"></i></p>
	      </div>
	    </a>
	  </div>
	</div>
	{% endfor %}
	</div>


	<h2>Videos</h2>

	<p>Workshops were held at the Universities of Bradford, Cambridge, Bournemouth and York, and were led by world-leading experts in fish analysis: Andrew Jones, James Barrett, Alison Locker, Shelia Hamilton-Dyer and Rebecca Nicholson. To capture and distil the expertise available at these events, all of the workshops were filmed and the resulting footage was cut together to produce a series of training e-lectures.</p>

	<a href="/videos.html" class="btn btn-primary">View videos <i class="fas fa-chevron-circle-right"></i></a>


</div>
