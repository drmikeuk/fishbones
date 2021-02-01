---
layout: default
title: "Families"
nav: "yes"
sortTitle: "c"
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
	<h2>Families</h2>
	<ul>
	<!-- 'map' so only category property + 'uniq' to remove duplicates => simple list of cats -->
	{% assign cats = site.data.fishbones | map: "Family"| uniq | sort  %}
	{% for cat in cats %}
		<!-- remove spaces + top & tail => /category/<thiscat>.html -->
		{% assign link = cat | remove: " " | prepend: "/Family/" | append: ".html" %}
		<li><a href="{{link}}">{{cat | capitalize }}</a></li>
	{% endfor %}
	</ul>
</div>
