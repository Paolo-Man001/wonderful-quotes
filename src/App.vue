<template>
  <div class="container" id="app">
    <app-quote-grid :quotes="quotesArray"/>
  </div>
</template>

<script>
   import QuoteGrid from "@/components/QuoteGrid";

   export default {
      name: 'App',
      components: {
         appQuoteGrid: QuoteGrid,

      },
      data: function () {
         return {
            selectComponent: 'QuoteGrid',
            quotesArray: [
               'I am a sample Quote...',
               'I am a sample Quote...'
            ],
            maxQuotes: 10
         }
      }
   }
</script>

<style>
  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    /*text-align: center;*/
    /*color: #2c3e50;*/
    /*margin-top: 60px;*/
  }
</style>
