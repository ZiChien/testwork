<script setup lang="ts">
interface user{
    username:string
    email:string
    introduction:string
}
defineProps<{user:user}>()
</script>
<template>
<div class="profile">
    <div class="profileHeader">
        <div class="avater">
            <img src="@/assets/avater_default.png" alt="">
        </div>
        <div class="userInfo">
            <h2>{{user.username}}</h2>
            <h4>{{user.email }}</h4>
        </div>
    </div>
    <div class="profileIntro">
        <p>{{user.introduction }}</p>
    </div>
</div>
</template>
<style scoped>
.profile{
    padding: 20px 0;
}
.profileHeader{
    width: 80%;
    margin: auto;
    display: flex;
    justify-content: flex-start;
    align-items: center;
}
.avater{
    margin-right: 10px;
}
.avater img{
    width: 66px;
}
.userInfo{
    padding: 0 10px;
}
h1,h2,h3,h4,h6{
    margin: 0;
    margin-bottom: 8px;
    font-family: 'Lato', sans-serif;
    font-weight: 400;
}
p{
    font-family: 'Lato', sans-serif;
}
.profileIntro{
    width: 80%;
    margin: auto;
}
</style>