<template>
  <div class = 'card'>
    <div class = 'top'>
      <div class="profile"></div>
    </div>
    <div class = 'info'>
        <p class = 'name'> Mr. meow</p>
        <p class = 'job'> web developer</p>
    </div>
    <div class="socialMedia">
        <div v-for="(icon, index) in icons" :key="index" class="icon">
          <i :class="icon"></i>
        </div>
    </div>
    <div class = 'buttons'>
      <button class ='button'>Subscribe</button>
      <button class ='button'>Manage</button>
    </div>
    <div class ='likeComment'>
      <div v-for="(element, index) in likeCommentIcon" :key="index" :class= "{'section': true, 'sectionBorder' : index != 0 }" >
      <i :class="element.icon"></i>
      <i class="text">{{ element.text }}</i>
    </div>
      
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      icons: [
        "fab fa-facebook-f",
        "fab fa-twitter",
        "fab fa-instagram",
        "fab fa-linkedin-in",
      ],
      likeCommentIcon: [
        {
          icon: "fas fa-thumbs-up",
          text: '10k'
        },
        {
          icon: "fas fa-comment",
          text: '20k'
        },
        {
          icon: "fas fa-share",
          text: '30k'
        }
      ],
    };
  },
};
</script>


<style scoped>
.card {
  background-color: #E8ECD7;
  position: relative;
  width: 20vw;
  height: 50vh;
  box-shadow: 5px 5px 10px rgba(0, 0, 0, 0.5);
  border-radius: 30px;
}

.top {
  height: 25%;
  background-color: #47663B;
  display: flex;
  justify-content: center;
  align-items: center;
  border-top-left-radius: 30px;
  border-top-right-radius: 30px;
  margin-bottom: 0;
}

.top .profile {
  position: relative;
  margin-top: 15%;
  width: 100px;
  height: 100px;
  border-radius: 60px;
  background-image: url('/src/assets/profile.jpg');
  background-size: cover;
  background-position: center;
  /* overflow: hidden;  */
}


.top .profile::before {
  content: "";
  position: absolute;
  inset: 0;
  padding: 5px; /* Adjust thickness of the border */
  border-radius: inherit; /* Keeps it rounded */
  background: linear-gradient(45deg, #1F4529,#EED3B1); /* Adjust gradient colors */
  -webkit-mask: 
    linear-gradient(white 0 0) content-box, 
    linear-gradient(white 0 0);
  -webkit-mask-composite: xor;
          mask-composite: exclude;
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
  font-size: 14px; /* Adjust text size */
  font-family: 'Orbitron', sans-serif; /* Change font */
  font-weight: bold;
}
.name {
margin-top: 4%;
margin-bottom: 1%;
font-size: 20px; /* Adjust text size */
font-family: 'Orbitron', sans-serif;
font-weight: bold;
}
.socialMedia{
  
  height: 15%;
  display: flex;
  justify-content: center;
  align-items: center;
}
.socialMedia .icon{
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


button {
  width: 35%;
  height: 50%;
  background: #1F4529; 
  color: white;
  font-size: 18px;
  border: none;
  margin: auto;
  border-radius: 5px; 
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
  display: flex;
  justify-content: center;
  align-items: center;
}
.likeComment .sectionBorder{
  border-left: black solid 1px;
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
