<template layout>
    <div class="flex justify-between">
        <h1 class="text-4xl text-center text-black-900 mb-2">List of Offices</h1>

    </div>

    <hr>

    <table class="border-collapse w-full">
        <thead>
            <tr>
                <th class="p-3 font-bold uppercase bg-gray-200 text-gray-600 border-gray-300 hidden lg:table-cell">Serial #</th>
                <th class="p-3 font-bold uppercase bg-gray-200 text-gray-600 border-gray-300 hidden lg:table-cell">Name</th>
                <th class="p-3 font-bold uppercase bg-gray-200 text-gray-600 border-gray-300 hidden lg:table-cell">Building</th>
                <th class="p-3 font-bold uppercase bg-gray-200 text-gray-600 border-gray-300 hidden lg:table-cell">In-charge</th>
            </tr>
        </thead>
        <tbody>
            <tr v-for="office in offices" :key="office.id" class="bg-white lg:hover:bg-gray-100 flex lg:table-row flex-row lg:flex-row flex-wrap lg:flex-no-wrap mb-10 lg:mb-0">
                <td class="w-full lg:w-auto p3 text-gray-800 text-center border border-b block lg:table-cell relative lg:static">{{ ('00000000' + office.id) }}</td>
                <td class="w-full lg:w-auto p3 text-gray-800 text-center border border-b block lg:table-cell relative lg:static">{{ office.name }}</td>
                <td class="w-full lg:w-auto p3 text-gray-800 text-center border border-b block lg:table-cell relative lg:static">{{ office.building }}</td>
                <td class="w-full lg:w-auto p3 text-gray-800 text-center border border-b block lg:table-cell relative lg:static">{{ office.user.fullname }}</td>
            </tr>
        </tbody>
    </table>

</template>

<script setup>

defineProps({
    offices: Array
})
</script>
