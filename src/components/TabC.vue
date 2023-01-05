<script setup>
import { ref, reactive, onMounted, watchEffect } from "vue"
const name = ref('')
</script>

<template>
  <div>TabC content</div>

  <input type="text" v-model="name">

  <br>

{{ name }}
</template>
