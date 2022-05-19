<template>
    <div class="card">
            <img :src="album.poster" alt="">
            <h3>{{ album.title}}</h3>
            <p> {{ album.author}}</p>
            <p>{{ album.year}}</p>
    </div>
</template>

<script>
export default {
    name:"CardAlbum",
    props:{
        album:Object
    }
}

</script>

<style scoped lang="scss">
@import "../style/common.scss";

img{
    width:150px;
    margin:1rem 0;
}

h3{
    color:white;
    text-transform: uppercase;
    margin:1rem 0;
}

p{
    color:#817e7b;
}

</style>