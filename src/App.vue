<template>
    <div class="container">
      <!-- listen to quote added on this selector and then execute a new quote (can be called anything) -->
      <!-- i do get some data passed into newQuote from new quote vue file in the createNew function -->
      <app-new-quote @quoteAdded="newQuote"></app-new-quote>
      <!-- passing the array to the quote grid -->
      <app-quote-grid :quotes="quotes"></app-quote-grid>
    </div>
</template>

<script>
   import QuoteGrid from './components/QuoteGrid.vue';
   import NewQuote from './components/NewQuote.vue';

   export default {
       data: function () {
           return {
               quotes: [
                   'Just a Quote to see something'
               ],
               maxQuotes: 10
           }
       },
       methods: {
           newQuote(quote) {
              this.quotes.push(quote);
           }
       },
       components: {
           appQuoteGrid: QuoteGrid,
           appNewQuote: NewQuote
       }
   }
</script>

<style>
</style>
