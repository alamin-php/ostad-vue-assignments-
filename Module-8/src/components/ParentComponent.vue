<script setup>
      import ChildComponent from './ChildComponent.vue'  
      import { ref } from 'vue';
      const message  = ref("Hello from parent!");
</script>

<template>
    <h2 class="text-blue-700 text-xl my-5">Parent Component</h2>
    <p class="my-5">
        {{ message }}
    </p>
    <ChildComponent v-model="message"/>
</template>