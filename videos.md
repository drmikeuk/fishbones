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
	<div class="col-lg-4 col-md-6 col-sm-12 pb-4">
	  {% assign thumb = video.Filename | prepend: "/videoimages/" %}
	  <div class="tile">
	    <a href="{{ video.link }}">
	      <div class="tile" style="background-image: url({{thumb}})">
	        <p>{{ video.Title }} <i class="fas fa-chevron-circle-right"></i></p>
	      </div>
	    </a>
	  </div>
	</div>
	{% endfor %}
	</div>


</div>
