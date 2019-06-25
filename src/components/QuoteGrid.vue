<template id="">
  <div class="row">
<!-- the holder of the content for single quotes. I can loop through them to render the single quote for each loop and pass the content to it. -->
    <app-quote v-for="quote in quotes">
      {{ quote }}
    </app-quote>
  </div>

  </div>

</template>

<script>
import Quote from './Quote.vue';
// default object shall have some props named quotes which are passed from outside so that I have access to them
// with quotes available I can loop through them as soon as I have my quote component
  export default {
    props: ['quotes'],
    // registering the single quote vue file.
    components: {
      appQuote: Quote
    }
  }
</script>
