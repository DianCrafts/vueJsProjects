<template>
    <div class = "box" :style="{backgroundColor: creme, borderColor: darkGreen}">
            name
    </div>

</template>
  
  <script>
  export default {
    data(){
        return{
            creme: "#EED3B1",
            darkGreen: "#1F4529"
        }
    }
    

  };
  </script>
  
  <style>
  
  body, html {
    height: 100vh;
    
  }
  
  
  .box{
    height: 40px;
    border: 2px solid;
  }
  </style>
  