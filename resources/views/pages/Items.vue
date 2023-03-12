<template layout>
    <div class="py-4">
        <h1 class="text-4xl  text-black-900 mb-2">List of Items</h1>
    </div>

        <hr>
        
        <table class="border-collapse w-full">
            <thead>
                <tr>
                    <th class="p-3 font-bold uppercase bg-gray-200 text-gray-600 border-gray-300 hidden lg:table-cell">Serial #</th>
                    <th class="p-3 font-bold uppercase bg-gray-200 text-gray-600 border-gray-300 hidden lg:table-cell">Name</th>
                    <th class="p-3 font-bold uppercase bg-gray-200 text-gray-600 border-gray-300 hidden lg:table-cell">Description</th>
                    <th class="p-3 font-bold uppercase bg-gray-200 text-gray-600 border-gray-300 hidden lg:table-cell">Office</th>
                    <th class="p-3 font-bold uppercase bg-gray-200 text-gray-600 border-gray-300 hidden lg:table-cell">Value</th>
                    <th class="p-3 font-bold uppercase bg-gray-200 text-gray-600 border-gray-300 hidden lg:table-cell">Status</th>
                </tr>
            </thead>
            <tbody>
                <tr v-for="item of items" :key="item.id" class="bg-white lg:hover:bg-gray-100 flex lg:table-row flex-row lg:flex-row flex-wrap lg:flex-no-wrap mb-10 lg:mb-0">
                    <td class="w-full lg:w-auto p3 text-gray-800 text-center border border-b block lg:table-cell relative lg:static">{{ ('00000000' + item.id).slice(-8) }}</td>
                    <td class="w-full lg:w-auto p3 text-gray-800 text-center border border-b block lg:table-cell relative lg:static">{{ item.name }}</td>
                    <td class="w-full lg:w-auto p3 text-gray-800 text-center border border-b block lg:table-cell relative lg:static">{{ item.description }}</td>
                    <td class="w-full lg:w-auto p3 text-gray-800 text-center border border-b block lg:table-cell relative lg:static">{{ item.office.name }}</td>
                    <td class="w-full lg:w-auto p3 text-gray-800 text-center border border-b block lg:table-cell relative lg:static">{{ item.value }}</td>
                    <td class="w-full lg:w-auto p3 text-gray-800 text-center border border-b block lg:table-cell relative lg:static">{{ item.status }}</td>
                </tr>
            </tbody>
        </table>
</template>

<script setup>

defineProps({
    'items':Array
})

</script>
