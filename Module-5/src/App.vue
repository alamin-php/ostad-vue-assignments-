<script setup>
import { RouterView } from "vue-router";
</script>

<template>
  <section class="flex h-screen w-full">
    <div
      class="w-1/2"
      style="
        background-image: url(https://images.unsplash.com/photo-1529539795054-3c162aab037a?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1470&q=80);
        background-repeat: no-repeat;
        background-size: cover;
      "
    >
    </div>
    <RouterView />
  </section>
</template>
<style scoped></style>
