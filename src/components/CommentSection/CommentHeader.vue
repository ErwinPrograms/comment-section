<script setup>
import CommentUser from './CommentUser.vue';
import CreationDate from '../Common/CreationDate.vue';

const props = defineProps({
    user: {
        type: Object,
        required: true
    },
    createdAt: {
        type: String,
        required: true
    }
})
</script>

<template>
    <div>
        <CommentUser :user="user" />
        <CreationDate :createdAt="createdAt" />
    </div>
</template>