<template>
    <div class="container">
      <!-- passing the array to the quote grid -->
      <app-quote-grid :quotes="quotes"></app-quote-grid>
    </div>
</template>

<script>
import QuoteGrid from './components/QuoteGrid.vue';

// returns the data object
export default {
   data: function () {
       return {
           quotes: [
               'Just a Quote to see something'
           ],
           maxQuotes: 10
       }
   },
   components: {
       appQuoteGrid: QuoteGrid,
   }
}
</script>

<style>
</style>
