<template>
    <header class="bg-white shadow-md h-16 flex justify-between items-center">
        <router-link :to="{name: 'home'}" class="inline-flex items-center h-full px-5">
            Home
        </router-link>
        <div class="px-5">
            <router-link  :to="{name: 'byName'}" class="inline-block px-2 h-full hover:bg-gray-100 hover:rounded-xl hover:font-bold hover:duration-150">
                Search Meals
            </router-link>
            <router-link  :to="{name: 'byLetter'}" class="inline-block px-2 h-full hover:bg-gray-100 hover:rounded-xl hover:font-bold hover:duration-150">
                Meals by Letters
            </router-link>
            <router-link  :to="{name: 'byIngredient'}" class="inline-block px-2 h-full hover:bg-gray-100 hover:rounded-xl hover:font-bold hover:duration-150">
                Meals by Ingredients
            </router-link>
        </div>
    </header>
</template>
