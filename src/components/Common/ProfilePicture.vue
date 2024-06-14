<script setup>
const props = defineProps({
    username: {
      type: String,
      required: false  
    },
    sourcePNG: {
        type: String,
        required: false
    }
})
</script>

<template>
    <div>
        <img :src="sourcePNG" :alt="username">
    </div>
</template>