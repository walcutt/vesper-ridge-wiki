---
layout: page
title: Search
permalink: /search
---

<input type="text" id="search-input" placeholder="Search blog posts..">

<div id="results-container"></div>

<script src="https://unpkg.com/simple-jekyll-search@latest/dest/simple-jekyll-search.min.js"></script>

<script>
    window.simpleJekyllSearch = new SimpleJekyllSearch({
        searchInput: document.getElementById('search-input'),
        resultsContainer: document.getElementById('results-container'),
        json:'{{ site.baseurl }}/search.json',
        searchResultTemplate: '<div class="search-result-box"><a class="internal-link" href="{url}?query={query}" title="{desc}">{title}</a><br><div class="search-excerpt">{excerpt}</div></div>',
        // searchResultTemplate: '<li><a href="{url}?query={query}" title="{desc}">{title}</a></li>',
        noResultsText: '<div class="search-result-box">No results found</div>',
        limit: 10
    });
</script>