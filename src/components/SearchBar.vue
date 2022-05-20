<template>
    <div>
        <input type="text" placeholder="Caerca Album" v-model="searchWord">
        <button class="btn-cerca">Cerca</button>
        <button class="btn-reset">Reset</button>
    </div>
</template>

<script>
export default {
    name:"SearchBar",
    data:function(){
        return {
            searchWord:''
        }
    }
}
</script>

<style scoped lang="scss">
    div{
        color: white;
    }
</style>