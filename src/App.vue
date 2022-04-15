<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <Header />
  <Content />
  <Footer />
</template>

<script>
import Header from "./components/Header.vue"
import Content from "./components/Content.vue"
import Footer from "./components/Footer.vue"

export default {
  name: "App",
  components: {
    Header,
    Content,
    Footer
  }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 30px;
}
body {
  color: black;
}
header {
  background: #41b883;
  color: white;
}
footer {
  background: #35495e;
  color: white;
}
</style>
