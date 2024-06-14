<script setup>
import { inject } from 'vue'

const props = defineProps({
    author: {
        type: String,
        required: true
    }
})

const currentUser = inject('currentUser')
</script>

<template>
    <div v-if="currentUser.username != author">
        <span><img src="/icon-reply.svg" alt="reply"> Reply </span>
    </div>
    <div v-else>
        <span><img src="/icon-delete.svg" alt="delete"> Delete </span>
        <span><img src="/icon-edit.svg" alt="edit"> Edit </span>
    </div>
</template>