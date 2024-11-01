<script setup>

const charts = [
    {
        image: "https://gratisography.com/wp-content/uploads/2024/01/gratisography-cyber-kitty-800x525.jpg",
        title: "Golden age of 80s",
        creator: "Sean swadder",
        time: "2:34:45",
        inFav: false
    },
    {
        image: "https://letsenhance.io/static/8f5e523ee6b2479e26ecc91b9c25261e/1015f/MainAfter.jpg",
        title: "Reggae “n” blues",
        creator: "Dj YK mule",
        time: "1:02:42",
        inFav: true
    },
    {
        image: "https://letsenhance.io/static/03620c83508fc72c6d2b218c7e304ba5/11499/UpscalerAfter.jpg",
        title: "Tomorrow’s tunes",
        creator: "Obi Datti",
        time: "2:01:25",
        inFav: false
    },
]

</script>


<template>
    <div>
        <div class="flex flex-col gap-3">
            <div class="p-5 rounded-3xl flex justify-between items-center bg-[#1a1e1f]" v-for="chart in charts">
                <div class="flex gap-3 cursor-pointer">
                    <img :src="chart.image" alt="image" class="w-20 rounded-xl">
                    <div class="flex flex-col justify-between">
                        <h6 class="text-lg text-white">{{ chart.title }}</h6>
                        <span class="text-gray-100">{{ chart.creator }}</span>
                        <span class="text-white">{{ chart.time }}</span>
                    </div>
                </div>
                <Icon :name="chart.inFav ? 'solar:heart-angle-bold' : 'solar:heart-broken'" size="40"
                    class="text-white cursor-pointer hover:text-yellow-400"
                    :class="{ 'text-yellow-400': chart.inFav }" />
            </div>
        </div>
    </div>
</template>

<style scoped></style>