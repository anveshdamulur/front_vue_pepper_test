<template>
  <div class="app">
        <Register />
  </div>
</template>

<script>
import Register from "./components/Register";
export default {
  name: 'App',
  components: {
    Register
  }
}
</script>

<style>
*{

  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
:root{
    --black : #1b1b1b;
    --pink : #fff8e7;
    --silver : #b7b7b7;
    --orange : #ff9900;
}
#app {
  font-family: 'Rubik', sans-serif;;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
