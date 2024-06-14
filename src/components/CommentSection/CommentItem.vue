<script setup>
import CommentScore from './CommentScore.vue'
import CommentHeader from './CommentHeader.vue'
import CommentOptions from './CommentOptions.vue';
const props = defineProps({
    comment: {
        type: Object,
        required: true
    }
})
</script>

<template>
    <div>
        <CommentScore :score="comment.score" />
        <CommentOptions :author="comment.user.username"/>
        <CommentHeader :user="comment.user" :createdAt="comment.createdAt" />
        <p>
            <span v-if="comment.replyingTo"> @{{ comment.replyingTo }} </span>
            {{ comment.content }}
        </p>
    </div>
</template>

<style scoped>
div {
    background-color: hsl(0, 0%, 100%);
    width: 100%;
    height: auto;
}
</style>