<template>
  <div>
    <div class="container mt-5">
      <div class="row">
        <div
          v-for="movie of movies"
          :key="movie"
          class="card col-5 border-dark"
          style="width: 18rem;">
          <div class="caja"> <img class="card-img-top" :src="movie.image" /></div>

         
          <div class="card-body">
            <h5 class="card-title"> <a :href="movie.url"> {{ movie.title }}</a></h5>
            <p class="card-text">{{ movie.description }}</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import axios from "axios";

export default {
  name: "NewsCard",
  data() {
    return {
      movies: null,
    };
  },
  mounted() {
    axios
      .get(
        "https://gnews.io/api/v4/top-headlines?token=e6e3589416050f17d6f669dfcf8329ef&lang=es&max=4"
      )
      .then((response) => {
        this.movies = response.data.articles;
        console.log(this.movies);
      });
  },
};
</script>

<style scoped>
.card {
    margin: 10px auto;
}

 .caja {
    
    height: 300px;
    
}

.card img {
    height: 100%;
    width: 100%;
    object-fit: cover;
}
 
</style>
