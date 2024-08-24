<script setup>
import { ref, computed } from 'vue';
import movies from './data/movies.json';

const query = ref('');
const normalizedQuery = computed(() => query.value.toLowerCase());
const visibleMovies = computed(() => {
  return movies.filter(m => {
    return `${m.title}\n${m.description}`
      .toLowerCase()
      .includes(normalizedQuery.value);
  });
});
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
              v-model.trim="query"
            />
          </div>
        </div>
      </div>

      <div class="movies">
        <div
          class="card"
          data-cy="movie"
          v-for="movie of visibleMovies"
          :key="movie.imdbId"
        >
          <div class="card-image">
            <figure class="image is-4by3">
              <img
                data-cy="movie__image"
                :src="movie.imgUrl"
                :alt="movie.title"
              />
            </figure>
          </div>

          <div class="card-content">
            <div class="media">
              <div class="media-left">
                <figure class="image is-48x48">
                  <img src="./assets/images/imdb-logo.jpeg" alt="imdb" />
                </figure>
              </div>

              <div class="media-content">
                <p class="title is-8" data-cy="movie__title">
                  {{ movie.title }}
                </p>
              </div>
            </div>

            <div class="content">
              <p data-cy="movie__description">{{ movie.description }}</p>
              <a :href="movie.imdbUrl" data-cy="movie__link">IMDB</a>
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="sidebar">Sidebar goes here</div>
  </div>
</template>
