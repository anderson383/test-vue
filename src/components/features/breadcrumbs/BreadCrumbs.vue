
<script>

</script>

<template>
  <section class="bread-crumbs">
    <div class="container">
      <div class="list-bread">
        <a href="">Dashboard /</a>
      </div>
    </div>
  </section>
</template>

<style lang="scss">
  @import '../../../assets/modules/mixins';

  .bread-crumbs {
    background-color: #2D3339;
    
    @include media('mobile') {
      display: none;
    }
    .list-bread {
      margin-left: 4em;
      padding: 1.25em 0;
      a {
        color: #13B497;
        text-decoration: none;
      }
    }
  }
  
</style>  
