<template>
  <body class="bg">
  <div class="bg">
      <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
  </body>
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

<style scoped lang="css">
body, html {
  height: 100%;
}

.bg {
  background-image: url("https://mdbootstrap.com/img/Photos/Horizontal/Nature/full page/img(20).jpg");

  height: 70em;

  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
}
</style>
