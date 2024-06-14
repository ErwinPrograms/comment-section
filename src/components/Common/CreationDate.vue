<script setup>
const props = defineProps({
    createdAt: {
        type: String,
        required: true
    }
})
</script>

<template>
    <div> {{ createdAt }} </div>
</template>