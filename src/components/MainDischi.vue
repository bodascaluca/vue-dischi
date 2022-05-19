<template>
  <div class="container-main">

    
          <CardAlbum v-for="(item, index) in albums" :key="index" :album="item"/>
   

  </div>
</template>

<script>
import CardAlbum from "./CardAlbum.vue";
import axios from "axios";
export default {
    name:"MainDischi",
    components:{
         CardAlbum,
    },
    data:function(){
        return {
            mioAlbum: {
                poster: "",
                author: "Loris",
                title: "Il mio primo album",
                year: "2022"
            },
            albums:[]
        }
    },
    created(){
        axios.get("https://flynn.boolean.careers/exercises/api/array/music")
        .then((resp)=>{
            console.log(resp.data.response);
            this.albums = resp.data.response;
        })
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
        height:300px;
        border:1px solid yellow;
        margin: 5px 4px;
        text-align:center;
        background-color:#2d3b46 ;

    }

}

</style>