<script setup>

</script>

<template>
    <div>
        <div class="flex flex-col-reverse lg:flex-row p-5 lg:p-10 rounded-3xl bg-[#1a1e1f] gap-5 cursor-pointer">
            <div class="w-full lg:w-1/2 flex flex-col gap-5 lg:justify-between h-96">
                <span class="text-white">Currentd playlist</span>
                <div>
                    <h1 class="text-2xl font-bold text-white">R & B hist</h1>
                    <p class="text-gray-300 text-wrap line-clamp-6">Lorem ipsum dolor sit, amet consectetur adipisicing
                        elit. Ea,
                        consequatur
                        consequuntur? Similique
                        ipsam, cupiditate accusantium temporibus beatae aliquid nisi quisquam? Lorem ipsum dolor sit
                        amet, consectetur adipisicing elit. Saepe nemo quaerat repellendus dolores cumque veritatis
                        consequuntur similique nam, molestias a aut deserunt dolorem! Qui, inventore reprehenderit! Aut,
                        facere. Deserunt explicabo, autem illo illum asperiores vitae odio non corporis nemo nihil? Quas
                        exercitationem quia dicta reprehenderit ea labore quibusdam dolor</p>
                </div>
                <div class="flex items-center gap-4">
                    <UAvatarGroup size="sm" :max="5">
                        <UAvatar src="https://avatars.githubusercontent.com/u/739984?v=4" alt="benjamincanac" />
                        <UAvatar src="https://avatars.githubusercontent.com/u/904724?v=4" alt="Atinux" />
                        <UAvatar src="https://avatars.githubusercontent.com/u/7547335?v=4" alt="smarroufin" />
                        <UAvatar src="https://avatars.githubusercontent.com/u/7547355?v=4" alt="Ali" />
                        <UAvatar src="https://avatars.githubusercontent.com/u/7547365?v=4" alt="Tural" />
                    </UAvatarGroup>
                    <Icon name="solar:heart-bold" size="20" class="text-yellow-500" />
                    <span class="text-yellow-500">33k Like</span>
                </div>
            </div>
            <div class="w-full lg:w-1/2">
                <img src="https://gratisography.com/wp-content/uploads/2024/10/gratisography-cool-cat-800x525.jpg"
                    alt="image" class="h-full rounded-3xl">
            </div>
        </div>
    </div>
</template>

<style scoped></style>