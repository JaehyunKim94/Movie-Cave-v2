<template>
  <div class="mx-auto" id="profile">
    
    <v-container>
      <h2>{{ username }}'s</h2>
      <v-row
        justify="center"
      >
        <v-col>

        </v-col>   
      </v-row>
    </v-container>
    
    
  </div>
</template>

<script>
// import jwtDecode from 'jwt-decode'
import { mapGetters } from 'vuex';
import router from '../router';
import axios from 'axios'

const HOST = process.env.VUE_APP_SERVER_HOST;

export default {
  name: "profile",
  
  data () {
    return {
      username: null,
      my_reviews: [],
      my_movies: [],
      reviews_info: [],
    }
  },

  components: {
  },

  methods: {
    getInfo() {
      this.username = sessionStorage.getItem('username')
      const token = sessionStorage.getItem('jwt')
      // const user_id = jwtDecode(token).user_id
      const options = {
        headers: {
          Authorization: `JWT ${token}`
        }
      }
      axios.get(HOST+'/api/v1/my_movies/', options)
    }
  }, 

  computed: {
    ...mapGetters(['isLoggedIn']),
  },

  created () {
    if (this.isLoggedIn) {
      this.getInfo()
    } else{
      router.push('/login')
    }
  }
};
</script>

<style>
</style>