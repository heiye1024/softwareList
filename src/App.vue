<template>
  <div id="app">
    <BG></BG>
    <Header></Header>
    <Toolbar></Toolbar>
    <ContentWrap></ContentWrap>
    <RightMenu></RightMenu>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'
import Header from './components/Header.vue'
import Toolbar from './components/Toolbar.vue'
import ContentWrap from './components/ContentWrap.vue'
import RightMenu from './components/RightMenu.vue'
import BG from './components/BG.vue'

@Component({
  components: { Header, Toolbar, ContentWrap, RightMenu, BG }
})
export default class App extends Vue {}
</script>

<style lang="less">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  position: relative;
  display: flex;
  flex-direction: column;
  box-shadow: 0 0 13px #ccc;
  margin: 7vh auto 0;
  padding: 0;
  overflow: hidden;
  max-width: 1200px;
  width: 96vw;
  max-height: 86vh;
  height: 730px;
  color: #000;
}
body {
  overflow-y: hidden;
  background: #eee;
}
a {
  text-decoration: none;
}
li {
  list-style: none;
}

@media
screen and (max-width:480px){
  #app{
    width: 100%;
    height: 100vh;
    max-height: 100vh;
    margin: 0;
    padding: 0;
  }
}
</style>
