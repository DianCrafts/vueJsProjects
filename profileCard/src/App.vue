<template>
  <div>
    <div class="cartArea">
      <CartComponent :showBox="showBox" :user = "users[chosenUserId]" @hideBox="hideBox"/>
    </div>
    <div class="nameBox">
      <BoxName v-for="(user, index) in users" :key="index" :name="user.name" @updateShowBox="updateShowBox(index)"></BoxName>
    </div>
  </div>

  
</template>

<script>

import BoxName from './components/BoxName.vue';
import CartComponent from './components/CartComponent.vue';

export default {
  components: {
    CartComponent,
    BoxName

  },
  data(){
    return{
      users : [{name: "name1", job: "job1"},{name: "name2", job: "job2"},{name: "name2", job: "job2"},{name: "name3", job: "job3"},{name: "name4", job: "job4"},{name: "name5", job: "job5"},{name: "name6", job: "job6"},{name: "name7", job: "job7"},{name: "name8", job: "job8"},],
      showBox: false,
      chosenUserId: -1
    }
  },
  methods:{
    updateShowBox(index){
      this.showBox = true
      this.chosenUserId = index
    },
    hideBox(){
      this.showBox = false
    }
  }
  
};
</script>

<style>

body, html {
 
  height: 100vh;
  
}

.nameBox{

  padding-top: 5%;
  display: grid;
  grid-template-columns: repeat(10, 1fr); /* 8 equal columns */
  gap: 20px;
}

.nameBox .box {
  transition: all 0.3s ease; /* Smooth transition for scaling */
}

.nameBox .box:hover {
  transform: scale(1.2); 
}

.nameBox .box:active  {
  transform: scale(1.5);
}

.cartArea {

  display: flex;
  justify-content: center;
}

</style>
