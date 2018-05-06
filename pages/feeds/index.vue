<template>
  <section class="feed">
    <div>
      <h2> Feed {{ feeds }}</h2>
    </div>
  </section>
</template>

<script>
import axios from 'axios'
export default {
  async asyncData({ app }) {
    const feeds = await app.$axios.$get('http://localhost:8080/feeds')
    return { feeds }
  }
  //asyncData (context) {
  //  return axios.get('http://icanhazip.com')
  //  .then((res) => {
  //    return { results: res }
  //  })
  // .catch((e) => {
  //    console.error('error:', e)
  //  })
  //}
}
</script>
