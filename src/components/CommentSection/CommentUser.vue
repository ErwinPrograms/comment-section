<script setup>
import ProfilePicture from '../Common/ProfilePicture.vue'

const props = defineProps({
    user: {
        type: Object,
        required: true
    }
})
</script>

<template>
    <div>
        <ProfilePicture :sourcePNG="user.image.png" />
        <div> {{ user.username }} </div>
    </div>
</template>