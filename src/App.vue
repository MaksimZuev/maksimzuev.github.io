<template>
  <HelloWorld msg="Welcome to my work"/>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

* {
  margin: 0;
  padding: 0;
}

body {
  width: 100%;
  min-height: 100vh;
  background: rgb(34, 193, 195);
  background: linear-gradient(
    339deg,
    rgba(34, 193, 195, 1) 0%,
    rgba(253, 187, 45)
  );
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
