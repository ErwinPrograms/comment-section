<script setup>
import { ref } from 'vue';
import json from './data.json'
import CommentList from './components/CommentSection/CommentList.vue';

const allComments = ref(json.comments)
const currentUser = ref(json.currentUser)
</script>

<template>
    <main>
        <CommentList :allComments="allComments" />
    </main>
</template>
