<script setup>
//Import Components Asynchronously
import {  defineAsyncComponent } from 'vue';
const NavBar = defineAsyncComponent(() => import('@/components/NavBar.vue'));
</script>

<template>
  <div class="bg-light min-h-screen">
    <NavBar />
    <main>
      <router-view />
    </main>
  </div>
</template>
