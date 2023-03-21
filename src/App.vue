<template>
  <div id="app">
    <Header></Header>
    <Sidebar></Sidebar>
    <Banner></Banner>
    <Announce></Announce>
    <Programme></Programme>
    <Footer></Footer>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Banner from './components/Banner.vue'
import Announce from './components/Announce.vue'
import Programme from './components/Programme.vue'
import Footer from './components/Footer.vue'
import Sidebar from './components/Sidebar'

export default {
  name: 'App',
  components: {
    Header,
    Banner,
    Announce,
    Programme,
    Footer,
    Sidebar
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
  box-sizing: border-box;
  margin: 0 auto;
  background-color: #eff3f8;
  color: #4a596f;
}
</style>
