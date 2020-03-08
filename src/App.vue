<template>
  <div id="app">
    <Header></Header>
    <Tabs></Tabs>
    <Footer></Footer>
  </div>
</template>

<script>
import '@/assets/sass/main.sass'
import Header from './components/Header'
import Tabs from './components/Tabs'
import Footer from './components/Footer'

export default {
  name: 'App',
  components: {
    Tabs,
    Header,
    Footer,
  }
}
</script>