---
layout: default
title: "Home"
nav: "yes"
sortTitle: "a"
---

<div class="container" style="padding-top: 2rem">
	<h1>Elements</h1>
	<div class="row">
	<!-- 'map' so only category property + 'uniq' to remove duplicates => simple list of cats -->
	{% assign Elements = site.data.fishbones | map: "Element"| uniq | sort  %}
	{% for Element in Elements %}
		{% include tile.html %}
	{% endfor %}
	</div>
</div>




<div class="container" style="padding-top: 2rem">
	<h1>Elements</h1>
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
	<h1>Common names</h1>
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
	<h1>Families</h1>
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
	<h1>Geographical Ranges</h1>
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
