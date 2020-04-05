<template>
  <div class="container" id="app">
    <section class="section">
      <app-new-quote @quoteAdded="newQuote"/>
      <hr>
      <app-quote-grid :quotes="quotesArray"/>
      <div class="columns">
        <div class="column ">
          <div class="notification  has-background-warning">notification: Click on a quote to delete!</div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
   import QuoteGrid from "@/components/QuoteGrid";
   import NewQuote from "@/components/NewQuote";

   export default {
      name: 'App',
      components: {
         appQuoteGrid: QuoteGrid,
         appNewQuote: NewQuote
      },
      data() {
         return {
            selectComponent: 'QuoteGrid',
            quotesArray: [],
            maxQuotes: 10
         }
      },
      methods: {
         newQuote( quote ) {
            this.quotesArray.push(quote);
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
