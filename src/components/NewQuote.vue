<template>
  <div class="column is-offset-one-quarter is-half">
    <label for="newQuote" class="label">Add Quote :</label>
    <div class="field">
      <div class="control has-icons-left">
          <textarea
                  id="newQuote"
                  class="textarea is-primary"
                  v-model="quote">
          </textarea>
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
</template>

<script>
   export default {
      name: "NewQuote",
      data() {
         return {
            quote: ''
         }
      },
      methods: {
         createNew() {
            this.$emit('quoteAdded', this.quote);
            this.quote = '';
         }
      }
   }
</script>

<style scoped>

</style>