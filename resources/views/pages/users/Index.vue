<template layout>

    <div class="flex justify-between">
        <h1 class="text-4xl text-black-900">List of Users</h1>
        <Link href="/users/create" class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded focus:shadow-outline mb-3">Create User</Link>
    </div>

    <hr>

    <table class="border-collapse w-full">
        <thead>
            <tr>
                <th class="p-3 font-bold uppercase bg-gray-200 text-gray-600 border-gray-300 hidden lg:table-cell">Serial #</th>
                <th class="p-3 font-bold uppercase bg-gray-200 text-gray-600 border-gray-300 hidden lg:table-cell">Name</th>
                <th class="p-3 font-bold uppercase bg-gray-200 text-gray-600 border-gray-300 hidden lg:table-cell">Designation</th>
                <th class="p-3 font-bold uppercase bg-gray-200 text-gray-600 border-gray-300 hidden lg:table-cell">Department</th>
            </tr>
        </thead>
        <tbody>
            <tr v-for="user of users" :key="user.id" class="bg-white lg:hover:bg-gray-100 flex lg:table-row flex-row lg:flex-row flex-wrap lg:flex-no-wrap mb-10 lg:mb-0">
                <td class="w-full lg:w-auto p3 text-gray-800 text-center border border-b block lg:table-cell relative lg:static">{{ ('00000000' + user.id).slice(-8) }}</td>
                <td class="w-full lg:w-auto p3 text-gray-800 text-center border border-b block lg:table-cell relative lg:static">{{ user.fullname }}</td>
                <td class="w-full lg:w-auto p3 text-gray-800 text-center border border-b block lg:table-cell relative lg:static">{{ user.designation }}</td>
                <td class="w-full lg:w-auto p3 text-gray-800 text-center border border-b block lg:table-cell relative lg:static">{{ user.department }}</td>
            </tr>
        </tbody>
    </table>

</template>

<script setup>
import {Link} from '@inertiajs/inertia-vue3'

defineProps({
    'users': Array
})
</script>
