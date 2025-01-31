<template>
  
  <div class = 'card'>
    <div class = 'top'>
      <div class="profile"></div>
    </div>
    <div class = 'info'>
        <p class = 'name'> Mr. meow</p>
        <p class = 'job'> web developer</p>
    </div>
    <div class ='socialMedia'>
      <div class="icon"></div>
      <div class="icon"></div>
      <div class="icon"></div>
      <div class="icon"></div>
    </div>
    <div class = 'buttons'>
      <button class ='button'>Subscribe</button>
      <button class ='button'>Manage</button>
    </div>
    <div class ='likeComment'>
      <div class = 'section'>
        <div class="icon"></div>
        <div class="text">60.4k</div>
      </div>
      <div class = 'section'>
        <div class="icon"></div>
        <div class="text">20k</div>
      </div>
      <div class = 'section'>
        <div class="icon"></div>
        <div class="text">12.4k</div>
      </div>
    </div>
  </div>
</template>

<script>


export default {
  
}
</script>

<style>

body, html {
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  margin: 0;
}

.card {
  position: relative;
  width: 20vw;
  height: 50vh;
  box-shadow: 5px 5px 10px rgba(0, 0, 0, 0.5);
  border-radius: 30px;
}

.top {
  height: 25%;
  background-color: blue;
  display: flex;
  justify-content: center;
  align-items: center;
  border-top-left-radius: 30px;
  border-top-right-radius: 30px;
  margin-bottom: 0;
}

.top .profile{
  margin-top: 15%;
  background-image: url('/src/assets/profile.jpg');
  background-size: cover;
  width: 100px;
  height: 100px;
  max-width: 100px;
  max-height: 100px;
  border-radius: 50px;
  background-color: white;
}
.info {
  margin-top: 10%;
  flex-direction: column;
  display: flex;
  justify-content: center;
  align-items: center;
}
.job{
  margin: 1%;
  margin-bottom: 5%;
}
.name {
margin-top: 4%;
margin-bottom: 1%;
}
.socialMedia{
  background-color: white;
  height: 15%;
  display: flex;
  justify-content: center;
  align-items: center;
}
.socialMedia .icon{
  background-image: url('/src/assets/telegram.png');
  background-size: cover;
  width: 35px;
  height: 30px;
  max-width: 30px;
  max-height: 30px;
  margin-right: 2%;
}
.buttons{
  height: 15%;
  display: flex;
  justify-content: center;
  align-items: center;
}
.button {
  width: 35%;
  height: 50%;
}
.likeComment{
  height: 15%;
  display: flex;
  justify-content: center;
  align-items: center;
}

.likeComment .section{
  width: 30%;
  height: 80%;
  border-right: black solid 1px;
  display: flex;
  justify-content: center;
  align-items: center;
}
.likeComment .section .icon {
  background-image: url('/src/assets/like.png');
  background-size: cover;
  width: 30px;
  height: 30px;
  max-width: 30px;
  max-height: 30px;
  float: left;
}
.likeComment .section .text{
   float: right;
}

</style>
