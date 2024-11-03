<script setup>
</script>

<template>
    <div>
        <div class="w-full bg-[#1a1e1f] rounded-3xl p-5 flex flex-col-reverse lg:flex-row justify-between gap-10">
            <div class="flex flex-col justify-between lg:w-1/2 gap-5">
                <div class="flex flex-col gap-5">
                    <h6 class="text-3xl font-bold text-white">Offer For You</h6>
                    <p class="text-gray-400">Lorem ipsum dolor sit amet consectetur adipisicing elit. Aperiam dolor,
                        molestias reiciendis illum,
                        commodi maiores voluptatibus eos necessitatibus et debitis ducimus illo cupiditate. In maxime
                        nisi,
                        eos iusto fugiat eum nobis doloribus soluta debitis numquam reprehenderit cupiditate vitae
                        veniam
                        illo sapiente iure mollitia facere quisquam magni esse placeat veritatis quaerat.</p>
                </div>
                <UButton label="Get More" size="xl" class="justify-center bg-yellow-600 hover:bg-yellow-700"
                    trailing-icon="solar:alt-arrow-right-broken" />
            </div>
            <div class="lg:w-1/2 bg-cover overflow-hidden relative w-full h-96 rounded-3xl shadow-2xl ">
                <img src="https://static.vecteezy.com/system/resources/previews/037/044/052/non_2x/ai-generated-studio-shot-of-black-headphones-over-music-note-explosion-background-with-empty-space-for-text-photo.jpg"
                    alt="image" class="hover:scale-110 transition-all delay-25 h-full w-full" title="image">
            </div>
        </div>
    </div>
</template>

<style scoped></style>