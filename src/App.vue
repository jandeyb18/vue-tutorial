<script setup>

</script>

<template>
    <div class="bg-gray-200 h-full">
        <header class="bg-white shadow-md h-16 flex justify-between items-center">
            <router-link :to="{name: 'home'}">
                Home
            </router-link>
            <div>
                <router-link  to="/" class="inline-block px-2 h-full hover:bg-gray-100 hover:rounded-xl">
                    Search Meals
                </router-link>
                <router-link  to="/" class="inline-block px-2 h-full hover:bg-gray-100 hover:rounded-xl">
                    Meals by Letters
                </router-link>
                <router-link  to="/" class="inline-block px-2 h-full hover:bg-gray-100 hover:rounded-xl">
                    Meals by Ingredients
                </router-link>
            </div>
        </header>

        <main>
            <router-view />
        </main>
    </div>
</template>

<style scoped>

</style>
