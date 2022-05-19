<template>
    <div>
        <h1>
            Ci sono {{ albums}} Albums
        </h1>
    </div>
</template>

<script>
export default {
    name:"NumbersAlbums",
    props:{
        albums:Number
    }
}
</script>

<style scoped lang="scss">

    h1{
        color:white;
    }
</style>