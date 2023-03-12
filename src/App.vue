<template>
  <div id="app">
    <Header></Header>
    <Banner></Banner>
    <Announce></Announce>
    <Programme></Programme>
    <Footer></Footer>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Banner from './components/Banner.vue'
import Announce from './components/Announce'
import Programme from './components/Programme.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Header,
    Banner,
    Announce,
    Programme,
    Footer
  }
}
</script>

<style>
a {
  color: #4a596f;
  text-decoration: none
}

img {
  border: 0;
  vertical-align: middle;
}
ul,
ol {
  list-style: none;
}
#app {
  background-color: #eff3f8;
  color: #4a596f;
}
</style>
