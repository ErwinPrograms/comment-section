<script setup>
    const props = defineProps({
    score: {
        type: Number,
        required: true
    }
})
</script>

<template>
    <div>
        <span><img src="/icon-plus.svg" alt="plus"></span>
        <span> {{ score }} </span>
        <span><img src="/icon-minus.svg" alt="minus"></span>
    </div>
</template>