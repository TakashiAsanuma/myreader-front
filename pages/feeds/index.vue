<template>
  <section class="feed">
    <div>
      <h2> Feed </h2>
      <div v-for="feed in feeds" :key="feed.id">
      <article>
      <dl>
        <dt><a v-bind:href="feed.url">{{ feed.title }}</a></dt>
          <dd>
            {{ feed.site_name }}
          </dd>
          <dd>{{ feed.summary }}</dd>
      </dl>
      </article>
      </div>
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
