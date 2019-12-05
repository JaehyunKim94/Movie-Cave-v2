<template>
  <div class="movie-list">
    
    <v-row>
      <v-col v-for="movie in movies" :key="movie.id" cols="3">
        <MovieCard :movie="movie" />
      </v-col>
      
    </v-row>
  </div>
</template>

<script>
import MovieCard from '@/components/MovieCard'
export default {
  name:'MovieList',
  props: {
    movies: {
      type: Array,
    }
  },
  components: {
    MovieCard,
  }
}
</script>

<style>

</style>