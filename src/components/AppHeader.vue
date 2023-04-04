<script>

import {store} from '../store.js';

export default {
    name: "AppHeader",

    data() {
        return{

        }
    },
}
</script>

<template>
   <div id="search">

    <input v-model="store.searchText" type="text" placeholder="Inserisci il titolo del film">
    <button>Cerca</button>

    

   </div>
</template>

<style lang="scss" scoped>

#search{
    display: flex;
    gap: 10px;

}
    
</style>

