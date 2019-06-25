<template id="">
  <div class="col-sm-6 col-md-4 col-lg-3">
    <div class="panel panel-default">
      <div class="panel-body quote">
        <!-- the quote content should come from outside. this is the place where it will be rendered. -->
        <slot></slot>
      </div>
    </div>
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
