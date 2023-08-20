<script setup>
 const propsValue  = defineProps(['modelValue'])
 defineEmits(['update:modelValue'])

 function messageEmitted(){
     return 'Message change from child';  
 }
</script>
<template>
       <h3 class="text-blue-700 text-xl my-5">Child Component</h3>
       <p class="my-5">
         {{ modelValue }}
      </p>
      <button class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded my-5 w-48" @click="$emit('update:modelValue', messageEmitted())">
         Button
       </button>
</template>