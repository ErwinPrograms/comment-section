<script setup>
import CommentChain from './CommentChain.vue';
const props = defineProps({
    parentComments: {
        type: Object,
        required: true
    }
})
</script>

<template>
    <div class="comment-list">
        <div v-for="(parentComment, index) in parentComments" :key="index">
            <CommentChain :parentComment="parentComment" />
        </div>
    </div>
</template>

<style scoped>
    div.comment-list {
        width: 100%;
        height: 100%;
    }
</style>