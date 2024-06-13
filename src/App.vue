<script setup>
import { ref } from 'vue';
// Placeholder fetching data from a json file
import json from './data.json'
import CommentList from './components/CommentSection/CommentList.vue';

const data = ref(json)
const currentUser = ref(json.currentUser)
const allComments = ref(json.comments)
</script>


<template>
    <main>
        <div v-for="(value, key) in currentUser"> {{ key }} : {{ value }} </div>
        <!-- <div v-for="comment in allComments">
            <div v-for="(value, key) in comment"> {{ key }} : {{ value }} 
                <template v-if="key == 'replies'">
                    <div v-for="reply in value"> {{ reply }} </div>
                </template>
            </div>
        </div> -->
        <CommentList :allComments="allComments"/>
    </main>
</template>