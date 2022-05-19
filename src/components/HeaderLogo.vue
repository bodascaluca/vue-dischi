<template>
    <section>

        <div class="container-logo">
            <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/1/19/Spotify_logo_without_text.svg/768px-Spotify_logo_without_text.svg.png" alt="Logo Spotify">
        </div>

  </section>
</template>

<script>
export default {
    name:"HeaderLogo",
    props:{
        charactersNumber:Number
    }
}
</script>

<style lang="scss" scoped>
@import "../style/common.scss";

section{

    display: flex;
    align-items: center;
    img{
        width:50px;
        margin-left:2rem ;
    }
}
</style>