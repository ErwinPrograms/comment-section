<script setup>
const props = defineProps(['allComments'])
</script>

<template>
    <h1>Hi, I'm CommentList</h1>
    <div v-for="comment in allComments">
        <div v-for="(value, key) in comment"> {{ key }} : {{ value }} </div>
    </div>
</template>

