<template>
  <div class="container">
    <div class="inner">
      <MovieItem
        v-for="hello in movies"
        :key="hello.imdbID" 
        :movie="hello" />
    </div>
  </div>
</template>

<script>
import MovieItem from '~/components/MovieItem'

export default {
  components: {
    MovieItem
  },
  computed: {
    movies() {
      return this.$store.state.movie.movies
    }
  }
}
</script>