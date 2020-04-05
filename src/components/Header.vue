<template>
  <div class="columns">
    <div class="column is-full">
      <h3>Quotes Added : {{ quoteCount }} / {{ maxQuotes }}</h3>
      <progress class="progress progress-bar is-link show-value" :value="quoteCount" max="10">
<!--        {{ quoteCount }} / {{ maxQuotes }}-->
      </progress>
    </div>
  </div>
</template>

<script>
   export default {
      name: "Header",
      props: [ 'quoteCount', 'maxQuotes' ]

   }
</script>

<style scoped>
  .progress::-webkit-progress-value {
    transition: width 0.5s ease;
  }


</style>