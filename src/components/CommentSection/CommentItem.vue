<script setup>
import CommentScore from './CommentScore.vue'
import CommentHeader from './CommentHeader.vue'
const props = defineProps({
    comment: {
        type: Object,
        required: true
    }
})
</script>

<template>
    <div>
        <CommentScore :score="comment.score"/>
        <CommentHeader :user="comment.user" :createdAt="comment.createdAt" />
        <p> {{ comment.content }} </p>
    </div>
</template>

<style scoped>
    div {
        background-color: hsl(0, 0%, 100%);
        width: 100%;
        height: auto;
    }
</style>