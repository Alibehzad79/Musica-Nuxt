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
        <div class="cursor-pointer rounded-3xl p-5">
            <div class="flex flex-col gap-5 relative">
                <img :src="props.image" alt="image" @click="goToAlbum" class="w-full h-[20rem] rounded-3xl"
                    draggable="false">
                <div
                    class="flex items-center gap-2 absolute bottom-0 album-head rounded-3xl backdrop-blur-sm px-5 pb-1 w-full">
                    <div class="flex flex-col gap-1">
                        <NuxtLink :to="'/albums/' + props.title.replaceAll(' ', '-')"
                            class="text-xl font-bold text-white line-clamp-1">{{ title }}
                        </NuxtLink>
                        <span class="line-clamp-1 text-gray-200">{{ creator }}</span>
                    </div>
                </div>
                <Icon @click="null" name="solar:heart-broken" size="40"
                    class="cursor-pointer absolute mx-2 mt-1 right-0 text-white" />
            </div>
        </div>
    </div>
</template>

<style scoped></style>