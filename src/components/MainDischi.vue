<template>
  <div class="container-main">

      <div class="card">
          <ImgTitle />
      </div>

  </div>
</template>

<script>
import ImgTitle from "../components/ImgTitle.vue";
export default {
    name:"MainDischi",
    components:{
    ImgTitle,
    }
}
</script>

<style scoped lang="scss">
@import "../style/common.scss";

.container-main{
    border: 1px solid blue;
    width: 80%;
    margin: 0 auto;
    display:flex;
    flex-wrap: wrap;

    .card{
        width:calc(100% /5 - 8px);
        border:1px solid yellow;
        margin: 5px 4px;

    }

}

</style>