<script setup>

import { ref, onMounted } from 'vue';
import {apiProducts} from './services/neuapp.js';
import productsComponents from './components/productsComponents.vue'

const products = ref({})

onMounted(async ()=>{
  loadProdcuts()
})

async function loadProdcuts(){
  console.log("Vamos al dia");
  alert("vamos al dia")
  try {
    let response = await apiProducts()
    if(response.status == 200){
      products.value = response.data;

      console.log(response.data);
    }
  } catch (error) {
    console.log(error);
  }
}

</script>

<template>
  <productsComponents :products2="products.results"></productsComponents>
</template>

<style scoped>

</style>