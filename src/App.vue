<script setup>
import { ref } from 'vue';
import json from './data.json'
import CommentList from './components/CommentSection/CommentList.vue';

const parentComments = ref(json.comments)
const currentUser = ref(json.currentUser)
</script>

<template>
    <main>
        <CommentList :parentComments="parentComments" />
    </main>
</template>

<style scoped>
    main {
        background-color: hsl(223, 19%, 93%);
        height: 100vh;
        width: 100vw;
    }
</style>