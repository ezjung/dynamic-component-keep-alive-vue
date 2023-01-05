<script setup>
import { ref, reactive, onMounted, onActivated, onDeactivated } from "vue"

const name = ref('')

onMounted(() => {
  console.log('A is mounted')
})

onActivated(() => {
  console.log('A is activated')
})

onDeactivated(() => {
  console.log('A is deactivated')
})

</script>

<template>
  <div>TabA content</div>

  <input type="text" v-model="name">

  <br>

  {{ name }}

</template>
