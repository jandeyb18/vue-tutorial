<template>
    <div class="flex flex-col p-8">
    <!-- <meals-by-name /> -->
    
        <div class="flex gap-2 mt-2 justify-center">
            <router-link :to="{name: 'byLetter', params: {letter}}" v-for="letter of letters" :key="letter">
            {{ letter }}
            </router-link>
        </div>
        
       <!-- <pre>{{ ingredients }}</pre> -->
    </div>   
</template>

<script setup>
import { computed, onMounted, ref } from 'vue';
import store from '../store'
import axiosClient from '../axiosClient.js'
import MealsByName from './MealsByName.vue';


const letters = 'ABCDEFGHIJKLMNOPQRSTUVWXYZ'.split("");
const ingredients = ref([])

onMounted(async () => {
    const response = await axiosClient.get('/list.php?i=list')
    console.log(response.data)
    ingredients.value = response.data
})

</script>