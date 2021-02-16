---
layout: default
title: "All bones"
nav: "yes"
sortTitle: "m"
filter: "yes"
---

<div class="container">

<div class="row title" style="padding-top: 3em">
	<div class="col">
		<h2>All bones</h2>
	</div>
	<div class="col-lg-3 col-md-3 col-sm-12">
	<form class="form-inline">
		 <input class="form-control" id="filterFish" type="text" placeholder="Filter...">
	</form>
	</div>
</div>



	<div class="row tiles">

{% for bone in site.data.fishbones %}

{% assign link = bone.Title | remove: " " | remove: "(" | remove: ")" | downcase | prepend: "/bones/"| append: ".html" %}
<div class="col-lg-3 col-md-6 col-sm-12 pb-4" >
    <div class="card flex-fill" >
    <img src="{{ bone.Filename | prepend: "/thumbs/"}}" class="card-img-top" alt="photo of {{ bone.Title }}">
    <div class="card-body">
      <p class="card-cat">{{ bone.Family }}</p>
      <h5 class="card-title">{{ bone.CommonName }}</h5>
      <p class="card-text">{{ bone.Element }}</p>
      <p class="card-text">{{ bone.View }}</p>
      <a href="{{ link }}" class="stretched-link"><i class="fas fa-chevron-circle-right fa-2x"></i></a>
    </div>
  </div>
</div>

{% endfor %}

	</div>
</div>
