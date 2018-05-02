<template>
  <section class="feed">
    <div>
      <h2> Feed {{ name }}</h2>
    </div>
  </section>
</template>

<script>
export default {
  asyncData (context) {
    // コンポーネントをロードする前に毎回呼び出されます
    return { name: 'World' }
  }
}
</script>
