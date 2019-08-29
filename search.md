---
layout: page
permalink: /search/
title: Search
---

<!-- Search input field -->
  <div class="main-search form-group mb-0 border-bottom">
  <div class="input-group">
    <input id="search" name="main_input" class="form-control border-0" placeholder="press / to search" type="text">
    <div class="input-group-append">
      <span class="input-group-text border-0"><i class="fa fa-search" aria-hidden="true"></i></span>
    </div>
  </div>
</div>

<!-- Search result container -->
<div id="results-container" class="search-results position-absolute">
      <ul id="results" class="search-results-ul card shadow border border-top-0">
      </ul>
</div>

<!-- Script pointing to search-script.js -->
<script src="search-script.js" type="text/javascript"></script>

<!-- Configuration -->
<script>
SimpleJekyllSearch({
  searchInput: document.getElementById('main_input'),
  resultsContainer: document.getElementById('results'),
  json: '/search.json'
})
</script>