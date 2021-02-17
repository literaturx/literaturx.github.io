---
layout: default
---

# literaturx

<!--p style="font-family: monospace">
{% assign pad0 = '00' %}
{% assign n = pad0 | size %}
{% assign m = 0 | minus: n %}
{% assign i = site.posts.size %}
{% for post in site.posts %}
	{% assign d = post.date | split: ' ' %}
	{% assign i = i | minus: 1 | prepend: pad0 %}
	{% assign j = i | slice: m, n %}
	{% assign k = d.first | replace: "-", "" %}
	[{{ j }}]
	<a href="{{ site.baseurl }}{{ post.url }}">
		{% comment %}
		{{ post.date | date: "%d-%b" }}
		{% endcomment %}
		{{ post.title }}</a>{% if j == "00" %}.{% else %},{% endif %}
{% endfor %}
</p-->

<!-- Html Elements for Search -->
<div id="search-container">
<input type="text" id="search-input" placeholder="search...">
<ul id="results-container"></ul>
</div>

<!-- Script pointing to search-script.js -->
<script src="/assets/js/simple-jekyll-search.min.js" type="text/javascript"></script>

<!-- Configuration -->
<script>
SimpleJekyllSearch({
  searchInput: document.getElementById('search-input'),
  resultsContainer: document.getElementById('results-container'),
  searchResultTemplate: '<a href="{url}" tabindex="1">{title}</a> • ',
  noResultsText: '<p>No results found!</p>',
  json: '/search.json',
})
</script>
