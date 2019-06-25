<template id="">
  <div class="row">
    <form class="" action="index.html" method="post">
      <div class="col-sm-8 col-sm-offset-2 col-xs-12 col-md-6 col-md-offset-3 form-group">
        <label for="">Quote</label>
        <!-- using v-model to bind whatever the user types in the text area to the quote object below  -->
        <!-- yay two way data binding -->
        <textarea name="name" rows="3" cols="80" v-model="quote" class="form-control"></textarea>
      </div>
      <div class="col-sm-8 col-sm-offset-2 col-xs-12 col-md-6 col-md-offset-3 form-group">
        <!-- prevent default behaviour. I don't want to submit the form or send the request to the server which would refresh the page. -->
        <!-- only execute the create new method -->
        <button type="button" name="button" @click="createNew.prevent" class="btn btn-primary">Add Quote</button>
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
    }
  },
  methods: {
    createNew() {
      // this quote will be updated all the time as we are binding it with two way binding therefore it should be reset after sending so the form gets cleared.
      this.$emit('quoteAdded', this.quote);
      this.quote = '';
    }
  }
}

</script>
