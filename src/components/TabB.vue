<script setup>
import { ref, reactive, onMounted, watchEffect } from "vue"

const name = ref('')

</script>

<template>
  <div>TabB content</div>

  <input type="text" v-model="name">

  <br>

  {{ name }}  
</template>
