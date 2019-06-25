<template>
    <div class="container">
      <app-new-quote></app-new-quote>
      <!-- passing the array to the quote grid -->
      <app-quote-grid :quotes="quotes"></app-quote-grid>
    </div>
</template>

<script>
import QuoteGrid from './components/QuoteGrid.vue';
import NewQuote from './components/NewQuote.vue';

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
   // register as a local component
   components: {
       appQuoteGrid: QuoteGrid,
       appNewQuote: NewQuote
   }
}
</script>

<style>
</style>
