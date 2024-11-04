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
]


</script>

<template>
    <div>
        <div class="flex items-center justify-between">
            <strong class="text-3xl text-white font-bold">Last albums</strong>
            <NuxtLink to="/albums">
                <UButton label="See more" variant="solid" color="yellow" size="lg">
                    <template #trailing>
                        <Icon name="solar:alt-arrow-right-bold-duotone" size="18" />
                    </template>
                </UButton>
            </NuxtLink>
        </div>
        <div class="grid grid-cols-1 md:grid-cols-3 mt-10 gap-10">
            <AlbumCard v-for="album in albums" :key="album" :image="album.image" :title="album.title"
                :creator="album.creator" :avatar="album.avatar" />
        </div>
    </div>
</template>

<style scoped></style>