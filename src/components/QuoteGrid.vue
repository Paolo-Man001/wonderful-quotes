<template>
  <section class="section">
    <app-new-quote/>
    <div class="columns is-multiline">
      <app-quote v-for="(quote,i) in quotes" :key="i">
        "{{ quote }}"
      </app-quote>
    </div>
  </section>
</template>

<script>
   import Quote from "@/components/Quote";
   import NewQuote from "@/components/NewQuote";

   export default {
      name: "QuoteGrid",
      components: {
         appQuote: Quote,
         appNewQuote: NewQuote
      },
      props: [ 'quotes' ]
   }
</script>

<style scoped>

</style>