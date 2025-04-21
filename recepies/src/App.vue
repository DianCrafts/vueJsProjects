<template>
  <div class="signupSection" :style="{background: purpleColor}" @click="signUp"> 
    <svg  class="inline-block w-3 h-3 mr-1 heart" viewBox="0 0 520 600" role="img" xmlns="http://www.w3.org/2000/svg">
<path d="M462.3 31.6C407.5 -15.1 326 -6.7 275.7 45.2L256 65.5L236.3 45.2C186.1 -6.7 104.5 -15.1 49.7 31.6C-13.1 85.2 -16.4 181.4 39.8 239.5L233.3 439.3C245.8 452.2 266.1 452.2 278.6 439.3L472.1 239.5C528.4 181.4 525.1 85.2 462.3 31.6V31.6Z" fill="#EBB454"></path>
</svg>
    Our recipes, your inbox. <span style="color: white;"> Sign up </span>
  </div>
  <div class="navigations">
    <nav>
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link> |
      <router-link to="/recepie">Recepie</router-link>
    </nav>
</div>


  <router-view/>
</template>

<script setup>
  const purpleColor = 'rgba(114, 63, 95, 1)'

  function signUp() {
  console.log("Hello from Composition API!");
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

html, body {
  margin: 0;
  padding: 0;
}

.heart{
  margin-right: 5px;
  height: 20px;
  width: auto;
}
.signupSection{
  cursor: pointer;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 25px;
  color: rgba(201, 177, 192, 0.9);
}


.navigations{
  height: 10%;
  width: 100%;
  border-bottom: 1px solid rgb(218, 201, 211);
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}
</style>
