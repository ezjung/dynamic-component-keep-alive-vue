<script setup>
import { ref, reactive, onMounted, onActivated, onDeactivated } from "vue"
const name = ref('')

onMounted(() => {
  console.log('C is mounted')
})

onActivated(() => {
  console.log('C is activated')
})

onDeactivated(() => {
  console.log('C is deactivated')
})

</script>

<template>
  <div>TabC content</div>

  <input type="text" v-model="name">

  <br>

{{ name }}
</template>
