<script setup>

const route = useRoute()

</script>

<template>
    <div>
        <div class="flex flex-col gap-10 mb-56">
            <div class="flex flex-col lg:flex-row gap-10 items-center p-5 justify-start">
                <img src="https://pixlr.com/images/generator/text-to-image.webp" alt="image"
                    class="w-full lg:h-[30rem] lg:w-[30rem] rounded-3xl" lazy="true">
                <div class="flex flex-col gap-5 justify-between lg:h-96">
                    <div class="flex flex-col gap-2">
                        <h1 class="text-white text-3xl">{{ route.params.name }}</h1>
                        <p class="text-gray-300">Lorem ipsum dolor, sit amet consectetur adipisicing elit. Quisquam
                            fugiat
                            deleniti vel officiis quam
                            nulla repellendus, harum iure hic provident odit, voluptates quia minima. Ipsum eligendi
                            excepturi
                            sint enim vitae!</p>
                    </div>
                    <UButton label="Add to collection" class="w-full lg:w-1/2 justify-center rounded-3xl bg-gray-800"
                        variant="soft" color="yellow" size="xl" icon="solar:gallery-favourite-bold" />
                </div>
            </div>
            <Player src="https://torkify.ir/wp-content/uploads/2023/07/Ismail-YK-Sekerim.mp3?_=1"
                image="https://pixlr.com/images/generator/text-to-image.webp" title="Sekerim"
                :subtitle="route.params.name" />
        </div>

    </div>
</template>
<style scoped></style>