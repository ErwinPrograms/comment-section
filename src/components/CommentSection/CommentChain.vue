<script setup>
import CommentItem from './CommentItem.vue';
const props = defineProps({
    parentComment: {
        type: Object,
        required: true
    }
})
</script>

<template>
    <div class="comment-chain">
        <CommentItem :comment="parentComment" />
        <CommentItem v-for="comment in parentComment.replies" :comment="comment"/>
    </div>
</template>