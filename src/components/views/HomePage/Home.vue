<script setup lang="ts">
import headerMenu from '@/components/layouts/headerMenu.vue';
import intro from '@/components/views/HomePage/intro.vue';
import postlist from '@/components/views/HomePage/postlist.vue';
const user = {
    username:'zchian__nnn',
    email:'test20@gmail.com',
    introduction:'黃子謙ZiChien╬═╬═╬═╬═╬═╬═╣☘️☘️'
}
interface Post{
    name:string
    src:string
}
let posts: Post[] = [
    {
        name:'img1',
        src:'https://res.cloudinary.com/chian/image/upload/v1673114002/54/ahqjtqrxru6un9jkt2ph.png'
    },
    {
        name:'img2',
        src:'https://res.cloudinary.com/chian/image/upload/v1673114116/54/z78uf1txrntubdculxck.png'
    },
    {
        name:'img3',
        src:'https://res.cloudinary.com/chian/image/upload/v1673114245/54/bpf5ib16v3y5oebw1reh.png'
    },
    {
        name:'img4',
        src:'https://res.cloudinary.com/chian/image/upload/v1673114354/54/hsu4dctga84itqmrjvhu.png'
    },
    {
        name:'img5',
        src:'https://res.cloudinary.com/chian/image/upload/v1673114611/54/gqnzgukaofobdxriflxs.png'
    },
    {
        name:'img6',
        src:'https://res.cloudinary.com/chian/image/upload/v1673114709/54/gj4x25wdmhxsmmhf4mft.png'
    },
    {
        name:'img7',
        src:'https://res.cloudinary.com/chian/image/upload/v1673114952/54/ytwgitlpeyzn7mud1rmj.png'
    },
    {
        name:'img8',
        src:'https://res.cloudinary.com/chian/image/upload/v1673115053/54/bnnnjxmzwlgq4ccfm6m3.png'
    },
    {
        name:'img9',
        src:'https://res.cloudinary.com/chian/image/upload/v1673115166/54/igwrqprur0o5xcyr8sx4.png'
    },
    

]
</script>
<template>
    <headerMenu />
    <intro :user="user" />
    <h2>Post</h2>
    <postlist :posts="posts"/>
</template>
<style scoped>
h2{
    margin: 10px 0;
    text-align: center;
    font-family: 'Lato', sans-serif;
    font-weight: 700;
    padding-top: 10px;
    border-top: 2px solid rgb(196, 196, 196, 0.6);
}
</style>