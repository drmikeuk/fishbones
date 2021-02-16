---
layout: default
title: "Common Names"
nav: "yes"
sortTitle: "b"
filter: "yes"
---

<!-- HEADER -->
<div class="home">
	<div class="container">

	</div>
</div>


<div class="container">

<div class="row title">
	<div class="col">
		<h2>Common names TEST</h2>
	</div>
	<div class="col-lg-3 col-md-3 col-sm-12">
	<form class="form-inline">
		 <input class="form-control" id="filterFish" type="text" placeholder="Filter...">
	</form>
	</div>
</div>


	<div class="row tiles rect">
	<!-- 'map' so only category property + 'uniq' to remove duplicates => simple list of cats -->
	{% assign cats = site.data.cnTEST  %}
	{% for item in cats %}
	  {% assign cat = item.cat  %}
		<div class="col-lg-3 col-md-6 col-sm-12 pb-4">
		  {% comment %} LINK: remove spaces + top & tail => /category/<thiscat>.html {% endcomment %}
		  {% assign thumb = cat | remove: " " | remove: "'" | downcase | prepend: "/commonnamethumbs/"| append: ".jpg" %}
		  {% assign link = cat | remove: " " | remove: "'" | downcase | prepend: "/CommonName/"| append: ".html" %}
		  <div class="tile">
		    <a href="{{ link }}">
		      <div class="tile" style="background-image: url({{thumb}})">
		        <p>{{ cat | capitalize }} <i class="fas fa-chevron-circle-right"></i></p>
		      </div>
		    </a>
		  </div>
		</div>
	{% endfor %}
	</div>

</div>
