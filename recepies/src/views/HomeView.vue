<template>
  <div class="mainOptionContainer">
    <div class="mainOption" v-for="(option, index) in mainFoodOptions" :key="index"> 
      <img class="mainOptionImage" :src="option.image"/>
      {{ option.name }}
    </div>
  </div>
  <div class="title">RECOMMENDATIONS</div>
  <div class="carouselWrapper">
  <button @click="scrollLeft" class="navButton">←</button>
  
    <div class="recommendations" ref="carousel">
      <div class="recommendedOption" v-for="(item, index) in recommentdations" :key="index">
        <div class="recommendationImage">
          <img :src="item.image"/>
        </div>
        <div class="recommendationName"> {{ item.name }}</div>
        <div class="recommendationDetail">Full Recepie</div>
      </div>
    </div>
  <button @click="scrollRight" class="navButton">→</button>
  </div>

  <div class="searchWrapper">
    <input placeholder="search here" class="searchBar" v-model="searchInput"/>
    <i class="fas fa-search search-icon" @click="searchFunction"></i>
  </div>
</template>


<script setup>
  import { ref } from 'vue';
  const mainFoodOptions = [{name: 'Quick and Easy', image: new URL('@/assets/quickAndEasy.jpg', import.meta.url).href}, {name: 'Salads', image: new URL('@/assets/salad.jpg', import.meta.url).href}, {name: 'Vegetarian', image: new URL('@/assets/vegeterian.jpg', import.meta.url).href},{name: 'Healthy', image: new URL('@/assets/healthy.jpg', import.meta.url).href},{name: 'Instant Pot', image: new URL('@/assets/mealprep.jpg', import.meta.url).href},{name: 'Vegan', image: new URL('@/assets/vegan.jpg', import.meta.url).href}, {name: 'Dinner', image: new URL('@/assets/dinner.jpg', import.meta.url).href}]
  const recommentdations = [{name: 'Quick and Easy', image: new URL('@/assets/quickAndEasy.jpg', import.meta.url).href}, {name: 'Salads', image: new URL('@/assets/salad.jpg', import.meta.url).href}, {name: 'Vegetarian', image: new URL('@/assets/vegeterian.jpg', import.meta.url).href},{name: 'Healthy', image: new URL('@/assets/healthy.jpg', import.meta.url).href},{name: 'Instant Pot', image: new URL('@/assets/mealprep.jpg', import.meta.url).href},{name: 'Vegan', image: new URL('@/assets/vegan.jpg', import.meta.url).href}, {name: 'Dinner', image: new URL('@/assets/dinner.jpg', import.meta.url).href}]

  const carousel = ref(null);
  const searchInput = ref('')

  function scrollLeft() {
    if (carousel.value) {
      carousel.value.scrollBy({ left: -carousel.value.offsetWidth / 3, behavior: 'smooth' });
    }
  }

  function scrollRight() {
    if (carousel.value) {
      carousel.value.scrollBy({ left: carousel.value.offsetWidth / 3, behavior: 'smooth' });
    }
  }

  function searchFunction() {
    console.log("search")
    searchInput.value = ''
  }
</script>

<style>

.mainOptionContainer{
  position: relative;
  display: flex;
  align-items: center;
  justify-content: center;
  border-bottom: solid 1px gray;
  width: 50%;
  margin-right: auto;
  margin-left: auto;

}

.mainOption {
  margin: 20px;
  display: flex;
  flex-direction: column;
}
.mainOptionImage{
  width: 100px;
  height: 120px;
  border-radius: 50px;
  object-fit: cover;
}

.title{
  margin-top: 3vh;
  font-size: 2rem;
  color: rgb(121, 82, 121);
}
.carouselWrapper {
  
  margin-right: auto;
  margin-left: auto;
  position: relative;
  display: flex;
  align-items: center;
  width: 60%;
  overflow: hidden;
}


.recommendations{
  display: flex;
  overflow-x: auto;
  position: relative;
  width: 100%;
  height: 40vh;
  border-bottom: solid 1px gray;
  scrollbar-width: none;
}


.recommendedOption {
  min-width: calc(100% / 3); /* Show 3 items at a time */
  box-sizing: border-box;
  padding: 0.5rem;
  flex-shrink: 0;
  
}
.recommendationImage {
  
  height: 80%;
  position: relative;
}

.recommendationImage img{
  height: 100%;
}


.recommendationName{
  margin-right: auto;
  margin-left: auto;
  position: relative;
  top: -5px;
  height: 7%;padding-top: 10px;
  background-color: orange;
  width: 50%;
}
.recommendationDetail{
  margin-right: auto;
  margin-left: auto;
  position: relative;
  /* top: -5px; */
  height: 7%;padding-top: 10px;
  background-color: orange;
  width: 50%;
}

.navButton {
  background: none;
  border: none;
  font-size: 2rem;
  cursor: pointer;
  padding: 0 1rem;
}

.searchWrapper {
  margin-top: 5vh;
  margin-right: auto;
  margin-left: auto;
  position: relative;
  display: flex;
  align-items: center;
  height: 5vh;
  width: 50%;

}


.searchBar{
  width: 90%;
  height: 80%;
  border-radius: 50px;
  border: 3px solid rgb(128, 92, 115);
}

.search-icon {
  color: gray;
  font-size: 2.5rem;
  margin-left: 2%;
}
</style>

