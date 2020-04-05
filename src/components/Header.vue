<template>
  <div class="columns">
    <column class="column is-full">
      <h3>Quotes Added</h3>
      <progress class="progress is-small is-link" value="" max="10"
                :style="{width: (quoteCount/maxQuotes) * 100 + '%'}">
        {{ quoteCount }} / {{ maxQuotes }}
      </progress>
    </column>
  </div>
</template>

<script>
   export default {
      name: "Header",
      props: [ 'quoteCount', 'maxQuotes' ],
      computed: {}
   }
</script>

<style scoped>

</style>