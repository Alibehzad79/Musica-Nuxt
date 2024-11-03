<script setup>

const albums = [
    {
        image: "https://gratisography.com/wp-content/uploads/2024/01/gratisography-cyber-kitty-800x525.jpg",
        title: "In Shadow",
        creator: "T-Dj"
    },
    {
        image: "https://letsenhance.io/static/8f5e523ee6b2479e26ecc91b9c25261e/1015f/MainAfter.jpg",
        title: "Darkness",
        creator: "Tural"
    },
    {
        image: "https://www.piclumen.com/wp-content/uploads/2024/10/piclumen-first-01.webp",
        title: "Love You",
        creator: "Arkin"
    },
]


</script>

<template>
    <div>
        <strong class="text-3xl text-white font-bold">Last albums</strong>
        <div class="grid grid-cols-1 md:grid-cols-3 mt-5 gap-10">
            <div class="flex flex-col w-full cursor-pointer rounded-3xl border border-gray-800 relative bg-cover overflow-hidden"
                v-for="album in albums">
                <img :src="album.image" alt="image" draggable="false"
                    class="w-full h-[18rem] lg:h-[25rem] rounded-3xl hover:scale-110 transition-all delay-50">
                <div class="flex flex-col gap-2 ps-5 pb-2 lg:pb-5 absolute bottom-0 backdrop-blur-sm w-full">
                    <NuxtLink :to="'/albums/' + album.title" class="text-white font-bold text-2xl line-clamp-1">{{
                        album.title }}
                    </NuxtLink>
                    <span class="text-gray-300">{{ album.creator }}</span>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped></style>