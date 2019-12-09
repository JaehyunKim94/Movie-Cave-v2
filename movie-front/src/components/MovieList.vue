<template>
  <div class="movie-list">
    <v-row>
      <v-col v-for="movie in movies" :key="movie.id" cols="3">
        <MovieCard :movie="movie" />
        <!-- <MovieDialog :movie="movie" /> -->
      </v-col>
      
    </v-row>
  </div>
</template>

<script>
import MovieCard from './MovieCard.vue'
// import MovieDialog from './MovieDialog'

export default {
  name:'MovieList',
  props: {
    movies: {
      type: Array,
    }
  },
  components: {
    MovieCard,
    // MovieDialog,
  }
}
</script>

<style>

</style>