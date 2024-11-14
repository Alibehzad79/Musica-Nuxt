<script setup>
const props = defineProps([
    "image",
    "title",
    "creator"
])
</script>

<template>
    <div>
        <div class="flex flex-col gap-2 justify-between cursor-grab h-80 rounded-3xl relative">
            <img :src="props.image" width="234" class="rounded-3xl object-cover h-full" draggable="false">
            <NuxtLink :to="'/singer/' + props.creator.replaceAll(' ', '-')" class="text-white font-medium select-none">
                {{
                    props.title }}</NuxtLink>
            <span class="text-gray-500 select-none">{{ props.creator }}</span>
            <Icon @click="null" name="solar:heart-broken" size="40"
                class="cursor-pointer absolute mx-2 mt-1 right-0 text-white" />
        </div>
    </div>
</template>

<style scoped></style>