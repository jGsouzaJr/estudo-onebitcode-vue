<script setup>

import {ref} from 'vue';
import Profile from './components/Profile.vue';
const isOpen = ref(true)

</script>

<!--
// import OptionsApi from './components/OptionsApi.vue'
// import MetodoSetup from './components/MetodoSetup.vue';
// export default {
// components:{
//   OptionsApi,
//   CompositonApi,
//   MetodoSetup
// }
// } -->

<template>
 <div>
  <input type="checkbox" v-model="isOpen" > {{ isOpen }}
   <Profile v-if="isOpen"/>
  <!-- <OptionsApi/> -->
  <!-- <MetodoSetup/> -->
 </div>
</template>

<style>
*{
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
body{
  background: #1c1a1d;
  color: #e5e5e5;
}
#app{
  font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
  min-height: 100vh;
  max-width: 40rem;
  margin: 0 auto;
  text-align: center;
}

a{
  color: #f64348;
}

</style>