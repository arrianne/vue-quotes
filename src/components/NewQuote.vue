<template id="">
  <div class="row">
    <form>
      <div class="col-sm-8 col-sm-offset-2 col-xs-12 col-md-6 col-md-offset-3 form-group">
        <label>Quote</label>
        <!-- using v-model to bind whatever the user types in the text area to the quote object below  -->
        <!-- yay two way data binding -->
        <textarea class="form-control" rows="3" v-model="quote"></textarea>
      </div>
      <div class="col-sm-8 col-sm-offset-2 col-xs-12 col-md-6 col-md-offset-3 form-group">
        <!-- prevent default behaviour. I don't want to submit the form or send the request to the server which would refresh the page. -->
        <!-- only execute the create new method -->
        <button class="btn btn-primary" @click.prevent="createNew">Add Quote</button>
      </div>
    </form>
  </div>

  </div>

</template>

<script>
   export default {
       data: function() {
           return {
               quote: ''
           };
       },
       methods: {
           createNew() {
               this.$emit('quoteAdded', this.quote);
               this.quote = '';
           }
       }
   }
</script>
