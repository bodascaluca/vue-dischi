<template>
  <div id="app">
    <div class="header">
      <HeaderLogo />
    </div>

    <div class="main">
      <div class="conteiner-dischi">
        <MainDischi />
      </div>
    </div>
  </div>
</template>

<script>
import HeaderLogo from "./components/HeaderLogo.vue";
import MainDischi from "./components/MainDischi.vue";

export default {
  name: 'App',
  components: {
    HeaderLogo,
    MainDischi
}
}
</script>

<style lang="scss">
@import "./style/common.scss";

  .header{
    height: 100px;
    background-color:#2d3b46;
    display: flex;
    align-items:center;
  }

  .main{
    height:calc(100vh - 100px);
    background-color:#1d2e3b;
    padding-top:2rem;
  }
</style>
