<script setup>
  import IconSearch from '../../icons/Search.vue'

</script>

<template>

  <div class="input">
    <input type="text" placeholder="Search here">
    <div class="search-icon">
      <IconSearch />
    </div>
  </div>
</template>

<style>
  .input {
    position: relative;
    height: max-content;
    width: 100%;
  }

  .input input {
    box-sizing: border-box;
    min-height: 3.5em;
    background-color: #1C2126;
    border: 1px solid #2F363D;
    padding: 0 2.1em;
    border-radius: 12px;
    height: 52px !important;
    width: 100%;
  }
  .input input,
  .input input::placeholder {
    color: #B9B9B9;
  }
  .input::before {
    content: '';
    position: absolute;
    margin: auto 0;
    top: 0;
    bottom: 0;
    width: 2px;
    left: 1.3em;
    height: 1.6em;
    background-color: #13B497;
  }

  .search-icon {
    height: max-content;
    position: absolute;
    right: 1.3em;
    margin: auto 0;
    top: 0;
    bottom: 0;
  }

</style>
