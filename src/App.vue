<template>
  <div id="app">
    <img src="./assets/logo.png">
    <nav>
      <router-link to="/">Home</router-link>
      <router-link to="/about">About</router-link>
    </nav>
    <transition name="slide" mode="out-in">
      <router-view/>
    </transition>
  </div>
</template>
<script>
export default {
  name: 'App',
};
</script>
<style>
  nav {
    margin-bottom: 30px;
  }
  #app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
  }
  .slide-enter {
    opacity: 0;
    transform: translateX(-20%);
  }
  .slide-enter-active {
    transition: all .3s;
  }
  .slide-leave-active {
    transition: all .3s;
    opacity: 0;
    transform: translateX(-20%);
  }
  .slide-leave {
    /*opacity: 1;*/
  }
  .slide-move{
    transition: transform .3s;
  }

</style>
