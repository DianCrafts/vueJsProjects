<template>
  <div class="mainOptionContainer">
    <div class="mainOption" v-for="(option, index) in mainFoodOptions" :key="index"> 
      <img class="mainOptionImage" :src="option.image"/>
      {{ option.name }}
    </div>
  </div>
  <div class="recommendations">
    <div class="recommendedOption" v-for="(item, index) in recommentdations" :key="index">
      <div class="recommendationImage"></div>
      <div class="recommendationName"> {{ item.name }}</div>
      <div class="recommendationDetail"></div>
    </div>
  </div>
</template>


<script setup>

  const mainFoodOptions = [{name: 'Quick and Easy', image: new URL('@/assets/quickAndEasy.jpg', import.meta.url).href}, {name: 'Salads', image: new URL('@/assets/salad.jpg', import.meta.url).href}, {name: 'Vegetarian', image: new URL('@/assets/vegeterian.jpg', import.meta.url).href},{name: 'Healthy', image: new URL('@/assets/healthy.jpg', import.meta.url).href},{name: 'Instant Pot', image: new URL('@/assets/mealprep.jpg', import.meta.url).href},{name: 'Vegan', image: new URL('@/assets/vegan.jpg', import.meta.url).href}, {name: 'Dinner', image: new URL('@/assets/dinner.jpg', import.meta.url).href}]
  const recommentdations = [{name: 'Quick and Easy', image: new URL('@/assets/quickAndEasy.jpg', import.meta.url).href}, {name: 'Salads', image: new URL('@/assets/salad.jpg', import.meta.url).href}, {name: 'Vegetarian', image: new URL('@/assets/vegeterian.jpg', import.meta.url).href},{name: 'Healthy', image: new URL('@/assets/healthy.jpg', import.meta.url).href},{name: 'Instant Pot', image: new URL('@/assets/mealprep.jpg', import.meta.url).href},{name: 'Vegan', image: new URL('@/assets/vegan.jpg', import.meta.url).href}, {name: 'Dinner', image: new URL('@/assets/dinner.jpg', import.meta.url).href}]
</script>

<style>

.mainOptionContainer{
  position: relative;
  display: flex;
  align-items: center;
  justify-content: center;

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

.recommendations{
   position: relative;
   width: 100%;
   height: 40vh;
   border-top: solid 1px gray;
   border-bottom: solid 1px gray;
}

</style>

