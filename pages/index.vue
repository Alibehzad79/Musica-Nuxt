<script setup>
useSeoMeta({
    title: "Home | Free Music"
})
</script>

<template>
    <div>
        <div class="lg:p-5 rounded-2xl mb-10 flex flex-col gap-10">
            <div class="flex flex-col lg:flex-row gap-10">
                <div class="w-full lg:w-2/3">
                    <CurrentPlaylist />
                </div>
                <div class="w-full lg:w-1/3 flex flex-col gap-5 mt-10 md:mt-0">
                    <h6 class="font-bold text-2xl text-white">Top charts</h6>
                    <Chart />
                </div>
            </div>
            <NewReleases />
            <LastAlbums />
            <Populars />
        </div>
    </div>
</template>

<style scoped></style>