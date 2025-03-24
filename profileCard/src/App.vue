<template>
  <div class="nameBox">
    <BoxName v-for="index, name in names" :key="index">{{ name }}</BoxName>
  </div>
</template>

<script>

import BoxName from './components/BoxName.vue';
// import CartComponent from './components/CartComponent.vue';


export default {
  components: {
    // CartComponent,
    BoxName
  },
  data(){
    return{
      names : ["name1", "name2", "name3","name1", "name2", "name3","name1", "name2", "name3","name1", "name2", "name3","name1", "name2", "name3","name1", "name2", "name3","name1", "name2", "name3","name1", "name2", "name3",]
    }
  }
  
};
</script>

<style>

body, html {
  height: 100vh;
  
}


.nameBox{
  display: grid;
  grid-template-columns: repeat(10, 1fr); /* 8 equal columns */
  gap: 10px;
}
</style>
