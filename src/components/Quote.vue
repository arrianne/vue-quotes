<template id="">
  <div class="row">

  </div>

  </div>

</template>

<script>
// default object shall have some props named quotes which are passed from outside so that I have access to them
// with quotes available I can loop through them as soon as I have my quote component
  export default {
    props: ['quotes']
  }
</script>

<style media="screen">
  .panel-body {
    font-family: 'Arizonia', cursive;
    font-size: 24px;
    color: #6e6e6e;
  }

  .quote {
    cursor: pointer;
  }

  .quote:hover {
    background-color: #ffe2e2;
  }

</style>
