<script setup>
const props = defineProps([
    'title',
    'description',
    'singer'
])

</script>

<template>
    <div>
        <div class="shadow-xl p-3 flex flex-col gap-5">
            <NuxtLink :to="'/singer/' + singer.replaceAll(' ', '-')" class="text-xl font-bold text-blue-600">{{ title }}
            </NuxtLink>
            <p class="text-gray-400">{{ description }}</p>
            <span class="text-gray-100">
                <Icon name="solar:user-bold" /> {{ singer }}
            </span>
        </div>
    </div>
</template>

<style scoped></style>