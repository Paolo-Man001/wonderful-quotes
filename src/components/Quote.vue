<template>
  <div class="column is-one-fifth is-2-mobile">
    <div class="card is-link quote">
      <div class="card-content">
        <p class="subtitle has-text-white-ter">
          <!-- Single Quote's slot -->
          <slot></slot>
        </p>
      </div>
    </div>
  </div>
</template>

<script>
   export default {
      name: "Quote"
   }
</script>

<style scoped>
  .quote {
    cursor: pointer;
    background-color: #3273dc;
  }

  .quote:hover {
    background-color: #1fbc56
  }

  .card{
    box-shadow: 0 2px 3px 1px #7f90b9;
    border-radius: 8px 0;
  }
</style>