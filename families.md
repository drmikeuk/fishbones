---
layout: default
title: "Families"
nav: "yes"
sortTitle: "c"
filter: "yes"
---

<!-- HEADER -->
<div class="home">
	<div class="container">
		<div class="title">
			<h1>{{ title }}</h1>
		</div>
	</div>
</div>




<div class="container">

<div class="row title">
	<div class="col">
		<h2>Families</h2>
	</div>
	<div class="col-lg-3 col-md-3 col-sm-12">
	<form class="form-inline">
		 <input class="form-control" id="filterFish" type="text" placeholder="Filter...">
	</form>
	</div>
</div>


	<div class="row tiles rect">
	<!-- 'map' so only category property + 'uniq' to remove duplicates => simple list of cats -->
	{% assign cats = site.data.fishbones | map: "Family"| uniq | sort  %}
	{% for cat in cats %}
		<div class="col-lg-3 col-md-6 col-sm-12 pb-4">
		  {% comment %} LINK: remove spaces + top & tail => /category/<thiscat>.html {% endcomment %}
		  {% assign thumb = cat | capitalize | remove: " " | remove: "'" | prepend: "/familiesthumbs/"| append: ".jpg" %}
		  {% assign link = cat | downcase | remove: " " | prepend: "/Family/" | append: ".html" %}
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
