<script setup>
const props = defineProps({
    allComments: {
        type: Array,
        required: true
    }
})
</script>

<template>
    <div v-for="(comment, index) in allComments" :key="index">
        {{ comment }} 
    </div>
</template>