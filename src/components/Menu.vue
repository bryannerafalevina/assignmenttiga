<template>
    <div>
      <h3>Food Menu</h3>
      <h1> Most Popular Items</h1>
      <ul>
        <router-link>
          <Listmenu />
        </router-link>
      </ul>
    </div>
  </template>
  
  <script>
  import { ref } from 'vue';
  import Listmenu from '../components/ListMenu.vue'
  export default {
    name: 'Menu',
    setup() {
      const menu = ref([]);
  
      fetch('http://localhost:3000/dishes')
        .then((response) => response.json())
        .then((data) => {
          menu.value = data;
        });
  
      return { menu };
    },
  };
  </script>