

<template layout>

    <h1 class="text-4xl text-center text-black-900">Welcome To My Inventory!!!</h1>
    <p class="text-black-800">
        {{ message }}
    </p>
    
    

</template>

<script setup>

import { Link, usePage } from '@inertiajs/inertia-vue3'

const props = defineProps({
    topics:Array
})



const user = usePage().props.auth

console.log(user)

</script>
