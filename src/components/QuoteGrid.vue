<template>
  <section class="section">
    <div class="columns is-multiline">

        <Quote v-for="(quote,i) in quotes" :key="i">
          "{{ quote }}"
        </Quote>
    </div>
  </section>
</template>

<script>
   import Quote from "@/components/Quote";

   export default {
      name: "QuoteGrid",
      components: {
         Quote
      },
      props: [ 'quotes' ]
   }
</script>

<style scoped>

</style>