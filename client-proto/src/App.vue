<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div>
   <transition name="fade" mode ="out-in" enter-active-class="animated fadeIn slower-5s" leave-active-class="animated fadeOutDown slower-5s">
    <router-view></router-view>
    </transition>  
    </div>
</template>


<style>
@import "https://cdn.jsdelivr.net/npm/animate.css@3.5.1";
</style>


<style lang="scss">
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  // text-align: center;
  color: #2c3e50;
  // background-color: orange;
}
#nav {
  padding: 30px;
  a {
    font-weight: bold;
    color: #2c3e50;
    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
