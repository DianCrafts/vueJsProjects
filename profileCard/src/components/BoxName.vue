<template>
      <div class = "box" :style="{backgroundColor: creme, borderColor: darkGreen}" @click="updateShowBox">{{ name }}</div>
</template>
  
<script>

export default {
  
  data(){
      return{
          creme: "#EED3B1",
          darkGreen: "#1F4529"
      }
  },
  props: ['name'],
  methods:{
    updateShowBox() {
      console.log("^^^^^^^^")
      this.$emit('updateShowBox')
    }
  }

};
</script>

<style>
  
body, html {
  height: 100vh;
  
}


.box{
  display: flex;
  justify-content: center;
  align-items: center;
  height: 40px;
  border: 2px solid;
}


</style>
