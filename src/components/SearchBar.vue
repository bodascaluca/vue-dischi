<template>
    <div>
        <select v-model="searchWord" @change="$emit('searchClicked', searchWord)">
            <option value="Jazz">Jazz</option>
            <option value="Rock">Rock</option>
            <option value="Metal">Metal</option>
            <option value="Pop">Pop</option>
        </select>

        <!-- <button class="btn-cerca"
         @click="$emit('searchClicked', searchWord)"
        >Cerca</button> -->

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