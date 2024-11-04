<script setup>

const props = defineProps([
    "image",
    "title",
    "creator",
    "avatar",
])

const goToAlbum = () => navigateTo('/albums/' + props.title.replaceAll(' ', '-'))
</script>

<template>
    <div>
        <div class="shadow-md shadow-black cursor-pointer rounded-3xl p-5" @click="goToAlbum">
            <div class="flex flex-col gap-5">
                <img :src="props.image" alt="image" class="w-full h-[15rem] rounded-3xl" draggable="false">
                <div class="flex items-center gap-2">
                    <UAvatar :src="props.avatar" alt="avatar" size="xl" />
                    <div class="flex flex-col gap-1">
                        <NuxtLink :to="'/albums/' + props.title.replaceAll(' ', '-')"
                            class="text-xl font-bold text-white line-clamp-1">{{ title }}
                        </NuxtLink>
                        <span class="line-clamp-1 text-gray-600">{{ creator }}</span>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped></style>