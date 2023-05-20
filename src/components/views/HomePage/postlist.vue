<script setup lang="ts">
import { Image as VanImage } from 'vant';
import { computed } from 'vue';
interface Post {
    name: string
    src: string
}
const postlist = defineProps<{
    posts: Post[]
}>()
console.log(postlist.posts[0]);

const layoutPosts = computed(() => {
    console.log(postlist.posts.length);

    let tempList = [];
    let count = 0;
    for (let i = 0; i < Math.ceil(postlist.posts.length / 3); i++) {
        let each3postsArray = []
        for (let j = 0; j < 3; j++) {
            if (count + j < postlist.posts.length) {
                each3postsArray.push(postlist.posts[count+j])
            }
        }
        count+=3;
        tempList.push(each3postsArray);
        each3postsArray = [];
    }
    console.log(tempList);
    return tempList;
})

</script>
<template>
    <div class="postList">
        <div class="row" v-for="posts in layoutPosts">
            <div class="post" v-for="post in posts" :key="post.name">
                <van-image width="100%" :src="post.src" />
            </div>
        </div>
    </div>
</template>
<style scoped>
.postList {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
}

.row {
    width: 100%;
    display: flex;
    justify-content: flex-start;
    margin-bottom: 8px;
}

:deep(img) {
    width: 100%;
    border-radius: 10px;

}

:deep(img):hover {
    transition: 0.4s;
    opacity: 0.6;
}

.post {
    width: 31%;
    margin-left: 3%;
}

.post:first-child {
    margin-left: 0
}</style>