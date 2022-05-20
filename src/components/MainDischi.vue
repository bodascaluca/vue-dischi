<template>
<div>
    <div class="searchBar">
        <SearchBar />
    </div>
    <NumbersAlbums :albums="albums.length"/>
    <div v-if="loading"> 
    <TestDue />
    </div>
         <div v-else class="container-main">
                 <CardAlbum v-for="(item, index) in albums" :key="index" :album="item"/>
         </div>
   
</div>
</template>

<script>
import CardAlbum from "./CardAlbum.vue";
import TestDue from "./TestDue.vue";
import NumbersAlbums from "./NumbersAlbums.vue";
import SearchBar from "./SearchBar.vue";
import axios from "axios";


export default {
    name:"MainDischi",
    components:{
         CardAlbum,
         TestDue,
         NumbersAlbums,
         SearchBar
    },
    data:function(){
        return {
            mioAlbum: {
                poster: "",
                author: "Loris",
                title: "Il mio primo album",
                year: "2022"
            },
            albums:[],
            loading:true
        }
    },
    created(){
        axios.get("https://flynn.boolean.careers/exercises/api/array/music")
        .then((resp)=>{
            console.log(resp.data.response);
            this.albums = resp.data.response;
            this.loading = false;
        })
    }
}
</script>

<style scoped lang="scss">
@import "../style/common.scss";

.searchBar{
    display:flex;
    justify-content: space-around;
}

.container-main{
    width: 80%;
    margin: 0 auto;
    display:flex;
    flex-wrap: wrap;

    .card{
        width:calc(100% /5 - 8px);
        margin: 5px 4px;
        text-align:center;
        background-color:#2d3b46 ;
        font-size:.6rem;
    }

}

</style>