<template>
  <div id="app">
    <div class="header">
      <HeaderLogo />
    </div>

    <div class="main">
      <MainDischi />
    </div>
  </div>
</template>

<script>
import HeaderLogo from "./components/HeaderLogo.vue"
import MainDischi from "./components/MainDischi.vue"



export default {
  name: 'App',
  components: {
    HeaderLogo,
    MainDischi
}
}
</script>

<style lang="scss">

  .header{
    height: 100px;
    background-color:#2d3b46;
  }

  .main{
    height:calc(100vh - 100px);
    background-color:#1d2e3b;
  }
</style>
