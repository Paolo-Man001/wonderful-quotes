<template>
  <div class="columns is-multiline">
    <app-quote
            v-for="(quote,i) in quotes"
            :key="i"
            @click.native="deleteQuote(i)"
    >
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
      props: [ 'quotes' ],
      methods: {
         deleteQuote( index ) {
            this.$emit('quoteDeleted', index);
         }
      }
   }
</script>

<style scoped>

</style>