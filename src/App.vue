<template>
    <div class="container">
      <app-header :quoteCount="quotes.length" :maxQuotes="maxQuotes"></app-header>
      <!-- listen to quote added on this selector and then execute a new quote (can be called anything) -->
      <!-- i do get some data passed into newQuote from new quote vue file in the createNew function -->
      <app-new-quote @quoteAdded="newQuote"></app-new-quote>
      <!-- passing the array to the quote grid -->
      <app-quote-grid :quotes="quotes" @quoteDeleted="deleteQuote"></app-quote-grid>
      <div class="row">
           <div class="col-sm-12 text-center">
               <div class="alert alert-info">Info: Click on a Quote to delete it!</div>
           </div>
       </div>
    </div>
</template>

<script>
   import QuoteGrid from './components/QuoteGrid.vue';
   import NewQuote from './components/NewQuote.vue';
   import Header from './components/Header.vue';

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
             if(this.quotes.length >= this.maxQuotes){
               return alert('Please delete a quote first!')
             }
               this.quotes.push(quote);

           },
           deleteQuote(index) {
               this.quotes.splice(index, 1);
           }
       },
       components: {
           appQuoteGrid: QuoteGrid,
           appNewQuote: NewQuote,
           appHeader: Header
       }
   }
</script>



<style>
</style>
