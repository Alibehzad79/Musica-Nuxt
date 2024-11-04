<script setup>
const items = [
    {
        image: "https://i1.sndcdn.com/artworks-000085665757-7hwy8q-t500x500.jpg",
        title: "Sekerim benim",
        creator: "Ismail YK"
    },
    {
        image: "https://media.mehrnews.com/d/2020/03/16/4/3408886.jpg",
        title: "Annem",
        creator: "Mahsun Kirmizigül"
    },
    {
        image: "https://cdn1.kralmuzik.com.tr/media/content/21-09/22/aaaaaaaaaaaaaaaaaaaaaaa.jpg",
        title: "Sevgili",
        creator: "Aleyna Tilki"
    },
    {
        image: "https://e0.pxfuel.com/wallpapers/488/225/desktop-wallpaper-simge-sa%C4%9F%C4%B1n-%C5%9Eark%C4%B1lar-saga-ve-sanatc%C4%B1lar.jpg",
        title: "Pirenses",
        creator: "Simge"
    },
    {
        image: "https://media.mehrnews.com/d/2018/06/02/4/2796689.jpg",
        title: "Asq",
        creator: "Ilyas Yalcintas"
    },
    {
        image: "https://admin.biyografya.com/_docs/photos/ab508fb027168f30d1589c1387031b79.jpg",
        title: "Biyografya",
        creator: "Tarkan"
    },
    {
        image: "https://i1.sndcdn.com/artworks-lO5RPLzv4eAVUBNR-JtY7yw-t500x500.jpg",
        title: "Yaparim bilirsin",
        creator: "Ebru gundes"
    },
]

</script>

<template>
    <div>
        <div class="flex flex-col gap-5">
            <span class="text-2xl text-white font-bold">New releases</span>
            <div>
                <UCarousel v-slot="{ item }" :items="items" :ui="{ item: 'basis-1/1 md:basis-1/3 lg:basis-1/6 mx-2', default: {prevButton: {class: 'bg-yellow-500 hover:bg-yellow-500'}, nextButton: {class: 'bg-yellow-500 hover:bg-yellow-500'}},  }" arrows>
                    <MusicCard :title="item.title" :creator="item.creator" :image="item.image" />
                </UCarousel>
            </div>
        </div>
    </div>
</template>

<style></style>