<script setup>
// import movies from './data/movies.json';
</script>

<template>
  <div class="page">
    <div class="page-content">
      <div class="box" data-cy="search">
        <div class="field">
          <label for="search-query" class="label">Search movie</label>

          <div class="control">
            <input
              data-cy="search__field"
              id="search-query"
              class="input"
              placeholder="Type search word"
            />
          </div>
        </div>
      </div>

      <div class="movies">
        <!-- Copy movies here -->
      </div>
    </div>

    <div class="sidebar">Sidebar goes here</div>
  </div>
</template>
