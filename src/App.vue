<script setup lang="ts">
import { ref } from 'vue';
import SizeSelector from './components/SizeSelector.vue';

const selectedSize = ref('XL');


</script>  

<template>     
<h1> Selecione la talla: {{ selectedSize }} </h1>
<SizeSelector
  :selected-size="selectedSize"
  @onChangeSize="selectedSize = $event"
  />


</template>  


<style>
#app {   
  font-family: Avenir, Helvetica, Arial, sans-serif;   
  -webkit-font.smoothing: antialiased;   
  -moz-osx-font-smoothing: grayscale;   
  text-align: center;   color: #2c3e50;   
  margin-top: 60px; 
  }

  button {
    border-radius: 5px;
    border: none;
    cursor: pointer;
    margin-right: 5px;
    padding: 5px;
    width: 75px;
  }

  .active {
    background-color: black;
    color: white;
    transition: all .3s ease-out;
  }
</style>