<template>
  <div>
    <v-card class="mx-auto" max-width="360" max-height="480" @click="detail">
      <v-img :src="movie.img_url">
      </v-img>
    </v-card>
  </div>
</template>

<script>
export default {
  name: "MovieCard",
  props: {
    movie: {
      type: Object
    }
  },
  methods: {
    detail() {
      this.movie
    }
  }
};
</script>

<style>
</style>