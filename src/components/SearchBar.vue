<template>
    <div>
        <input type="text" 
        placeholder="Caerca Album" 
        v-model="searchWord">
        <!-- <button class="btn-cerca"
         @click="$emit('searchClicked', searchWord)"
        >Cerca</button> -->

                <!-- mandiamo un evento e quindi creiamo un methods  -->
         <button class="btn-cerca" @click="sendEvent" 
        >Cerca</button>
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
    },
    methodes:{
        sendEvent(){
            //F are varie operazion 
            //      Scelgo un nome e lo catturo nel padre @searchClicked
            this.$emit('searchClicked', this.searchWord);
        }
    }
}
</script>

<style scoped lang="scss">
    div{
        color: white;
    }
</style>