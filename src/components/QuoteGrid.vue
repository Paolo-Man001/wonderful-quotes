<template>
    <div class="columns is-multiline">
      <app-quote v-for="(quote,i) in quotes" :key="i">
        "{{ quote }}"
      </app-quote>
    </div>
</template>

<script>
   import Quote from "@/components/Quote";

   export default {
      name: "QuoteGrid",
      components: {
         appQuote: Quote
      },
      props: [ 'quotes' ]
   }
</script>

<style scoped>

</style>