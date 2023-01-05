<script setup>
import { ref, reactive, onMounted, watchEffect } from "vue"
import { RouterLink, RouterView } from 'vue-router'
import TabA from './components/TabA.vue'
import TabB from './components/TabB.vue'
import TabC from './components/TabC.vue'

const currentTab = ref('TabA')

// create an object key (doesn't need to be a ref)
const components = { TabA, TabB, TabC }

const switchTabs = (tab) => {

  currentTab.value = tab

}



</script>

<template>
  <div>
    <button @click="switchTabs('TabA')">TabA</button>
    <button @click="switchTabs('TabB')">TabB</button>
    <button @click="switchTabs('TabC')">TabC</button>
  </div>

  <br>

  <div>

    <keep-alive>
      <component :is="components[currentTab]" />
    </keep-alive>


  </div>



</template>
