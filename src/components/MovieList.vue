<template>
  <div class="container">
    <div class="inner">
      <div class="message">
        {{ message }}
      </div>
      <div class="movies">
        <MovieItem
          v-for="hello in movies"
          :key="hello.imdbID"
          :movie="hello" />
      </div>
    </div>
  </div>
</template>

<script>
import MovieItem from "~/components/MovieItem";

export default {
  components: {
    MovieItem,
  },
  computed: {
    movies() {
      return this.$store.state.movie.movies;
    },
    message() {
      return this.$store.state.movie.message;
    },
  },
};
</script>

<style lang="scss" scoped>
.container {
  .movies {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
  }
}
</style>