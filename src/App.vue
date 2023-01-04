<script setup>
import { ref, reactive, onMounted, watchEffect } from "vue"
import { RouterLink, RouterView } from 'vue-router'
import TabA from './components/TabA.vue'
import TabB from './components/TabB.vue'
import TabC from './components/TabC.vue'

const activeTab = ref('TabA')

const handleActiveTab = (tab) => {

  activeTab.value = tab
}



</script>

<template>
  <div>
    <button @click="handleActiveTab('TabA')">TabA</button>
    <button @click="handleActiveTab('TabB')">TabB</button>
    <button @click="handleActiveTab('TabC')">TabC</button>
  </div>

  <br>

  <div>
    <TabA v-if="activeTab==='TabA'" />
    <TabB v-if="activeTab==='TabB'" />
    <TabC v-if="activeTab==='TabC'" />

  </div>



</template>
