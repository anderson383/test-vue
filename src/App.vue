<script setup>
import { RouterLink, RouterView } from 'vue-router'
import Header from './components/features/header/Header.vue'
</script>

<template>
  <header>

    <div class="wrapper">
      <Header msg="You did it! xd" />
      
      <!-- <nav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/about">About</RouterLink>
      </nav> -->
    </div>
  </header>

  <RouterView />
</template>

<style scoped>

</style>
