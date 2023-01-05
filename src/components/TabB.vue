<script setup>
import { ref, reactive, onMounted, onActivated, onDeactivated } from "vue"

const name = ref('')

onMounted(() => {
  console.log('B is mounted')
})

onActivated(() => {
  console.log('B is activated')
})

onDeactivated(() => {
  console.log('B is deactivated')
})

</script>

<template>
  <div>TabB content</div>

  <input type="text" v-model="name">

  <br>

  {{ name }}  
</template>
