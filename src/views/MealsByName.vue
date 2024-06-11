<template>
    <div class="py-5 max-w-xl mx-auto">
        <input  type="text" 
                v-model="keyword"
                class="rounded borded-2 border-gray-200 w-full" 
                placeholder = "Search for meals"
                @change="SearchMeals"
                > 
    </div>

    <div class="grid grid-cols-1 md:grid-cols-3 gap-3 mx-5">
        <div v-for="meal of meals" :key="meal.idMeal">
            <img :src="meal.strMealThumb" :alt="strMeal">
            <h3>{{ meal.strMeal }}</h3>
            <div>
               <a :href="meal.strYoutube" target="_blank">YouTube</a>
               <router-link to="/">
                View
               </router-link>
            </div>
        </div>
    </div>
</template>

<script setup>

import { computed, ref } from 'vue';
import store from '@/store';
  
const keyword = ref('');
const meals = computed(() => store.state.searchedMeals);

function SearchMeals() 
{
    store.dispatch('searchMeals', keyword.value)
}
</script>