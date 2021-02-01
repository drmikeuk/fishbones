---
layout: default
title: "Common Names"
nav: "yes"
sortTitle: "b"
---

<!-- HEADER -->
<div class="home">
	<div class="container">

	</div>
</div>


<div class="container">
	<h2>Common names</h2>
	<ul>
	<!-- 'map' so only category property + 'uniq' to remove duplicates => simple list of cats -->
	{% assign cats = site.data.fishbones | map: "CommonName"| uniq | sort  %}
	{% for cat in cats %}
		<!-- remove spaces + top & tail => /category/<thiscat>.html -->
		{% assign link = cat | remove: " " | prepend: "/CommonName/" | append: ".html" %}
		<li><a href="{{link}}">{{cat | capitalize }}</a></li>
	{% endfor %}
	</ul>
</div>
