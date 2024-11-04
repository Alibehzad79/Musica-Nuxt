<script setup>

const albums = [
    {
        image: "https://gratisography.com/wp-content/uploads/2024/01/gratisography-cyber-kitty-800x525.jpg",
        title: "In Shadow",
        creator: "T-Dj",
        avatar: "https://avatars.githubusercontent.com/u/739984?v=4"
    },
    {
        image: "https://letsenhance.io/static/8f5e523ee6b2479e26ecc91b9c25261e/1015f/MainAfter.jpg",
        title: "Darkness",
        creator: "Tural",
        avatar: "https://avatars.githubusercontent.com/u/739884?v=4"
    },
    {
        image: "https://www.piclumen.com/wp-content/uploads/2024/10/piclumen-first-01.webp",
        title: "Love You",
        creator: "Arkin",
        avatar: "https://avatars.githubusercontent.com/u/739284?v=4"
    },
    {
        image: "https://img-cdn.pixlr.com/image-generator/history/65bb506dcb310754719cf81f/ede935de-1138-4f66-8ed7-44bd16efc709/medium.webp",
        title: "And You",
        creator: "MDH",
        avatar: "https://avatars.githubusercontent.com/u/739215?v=4"
    },
    {
        image: "https://fps.cdnpk.net/images/home/subhome-ai.webp?w=649&h=649",
        title: "Coin Baby",
        creator: "Mehmet",
        avatar: "https://avatars.githubusercontent.com/u/739283?v=4"
    },
    {
        image: "https://gratisography.com/wp-content/uploads/2024/03/gratisography-funflower-800x525.jpg",
        title: "NTH",
        creator: "IBO",
        avatar: "https://avatars.githubusercontent.com/u/7392344?v=4"
    },
    {
        image: "https://th.bing.com/th/id/OIG2.9O4YqGf98tiYzjKDvg7L",
        title: "Solid Singer",
        creator: "Eli",
        avatar: "https://avatars.githubusercontent.com/u/739214?v=4"
    },
]


</script>

<template>
    <div>
        <div class="mb-10">
            <strong class="text-3xl text-white font-bold">Albums</strong>
            <div class="grid grid-cols-1 md:grid-cols-3 lg:grid-cols-6 mt-10 gap-10">
                <AlbumCard v-for="album in albums" :key="album" :image="album.image" :title="album.title"
                    :creator="album.creator" :avatar="album.avatar" />
            </div>
        </div>
    </div>
</template>

<style scoped></style>