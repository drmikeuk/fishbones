---
layout: home
title: "Home"
nav: "yes"
sortTitle: "a"
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

	<p>{{ site.blurb }}</p>

	<h2>Browse by element</h2>
	<div class="row tiles">
	<!-- 'map' so only category property + 'uniq' to remove duplicates => simple list of cats -->
	{% assign Elements = site.data.fishbones | map: "Element"| uniq | sort  %}
	{% for Element in Elements %}
		{% include tile.html %}
	{% endfor %}
	</div>
</div>




<div class="container" style="padding-top: 2rem">
	<h3>Elements</h3>
	<ul>
	<!-- 'map' so only category property + 'uniq' to remove duplicates => simple list of cats -->
	{% assign cats = site.data.fishbones | map: "Element"| uniq | sort  %}
	{% for cat in cats %}
		<!-- remove spaces + top & tail => /category/<thiscat>.html -->
		{% assign link = cat | remove: " " | prepend: "/Element/" | append: ".html" %}
		<li><a href="{{link}}">{{cat | capitalize }}</a></li>
	{% endfor %}
	</ul>
</div>


<div class="container" style="padding-top: 2rem">
	<h3>Common names</h3>
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

<div class="container" style="padding-top: 2rem">
	<h3>Families</h3>
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

<div class="container" style="padding-top: 2rem">
	<h3>Geographical Ranges</h3>
	<ul>
	<!-- 'map' so only category property + 'uniq' to remove duplicates => simple list of cats -->
	{% assign cats = site.data.fishbones | map: "GeographicalRange"| uniq | sort  %}
	{% for cat in cats %}
		<!-- remove spaces + top & tail => /category/<thiscat>.html -->
		{% assign link = cat | remove: " " | prepend: "/GeographicalRange/" | append: ".html" %}
		<li><a href="{{link}}">{{cat | capitalize }}</a></li>
	{% endfor %}
	</ul>
</div>
