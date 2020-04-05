<template>
  <section class="section">
    <div class="column is-offset-one-quarter is-half">
      <div class="field">
        <div class="control">
          <input class="input is-primary" v-model="quote" type="text" placeholder="Enter a Quote...">
        </div>
      </div>
      <div class="field">
        <div class="control">
          <button class="button is-primary"
                  @click.prevent="createNew">
            Submit
          </button>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
   export default {
      name: "NewQuote",
      data: () => {
         return {
            quote: ''
         }
      },
      methods:{
         createNew() {

         }
      }
   }
</script>

<style scoped>

</style>