<script setup lang="ts">
import { library } from '@fortawesome/fontawesome-svg-core';
import { faMagnifyingGlass } from '@fortawesome/free-solid-svg-icons';
import { faSquarePlus } from '@fortawesome/free-regular-svg-icons';


import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome';

library.add(faSquarePlus,faMagnifyingGlass);
</script>
<template>
    <nav>
        <div class="oslogo">
            <img src="@/assets/logo.png" alt="">
        </div>
        <div class="toollist">
            <div class="tool">
                <font-awesome-icon icon="fa-regular fa-square-plus" style="color: #000000;" />
            </div>
            <div class="tool">
                <font-awesome-icon icon="fa-solid fa-magnifying-glass" style="color: #000000;" />
            </div>
            <div class="tool">
                <img class="avater" src="@/assets/avater_default.png" alt="">
            </div>
        </div>
    </nav>
</template>
<style scoped>
nav{
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 20px 5%;
}
.oslogo img{
    width: 80px;
}
.toollist{
    display: flex;
    justify-content: flex-end;
    align-items: center;
}
.tool{
    width: 30px;
    margin-left: 10px;
}
.tool svg{
    width: 70%;
    height: 100%;
}
.avater{
    width: 100%;
    border-radius: 50px;
    border: 2px solid black;
}
</style>