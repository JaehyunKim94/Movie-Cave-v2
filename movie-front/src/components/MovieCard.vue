<template>
  <div>
    <v-card class="mx-auto" max-width="360" max-height="480">
      <v-img class="white--text align-end" :src="movie.img_url">
        <v-card-actions>
          <v-row>
            <v-rating
              v-model="rating"
              background-color="white"
              color="yellow accent-4"
              dense
              half-increments
              hover
            ></v-rating>
          </v-row>
          
        </v-card-actions>
      </v-img>
    <v-col>
      <v-btn color="orange" text>Detail</v-btn>
      <v-btn color="red" text>Youtube</v-btn>
    </v-col>
    
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
  }
};
</script>

<style>
</style>