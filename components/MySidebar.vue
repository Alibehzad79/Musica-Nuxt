<script setup>

</script>
<template>
    <div class="fixed lg:left-5 hidden lg:flex">
        <div class="flex flex-col gap-5">
            <div class="flex flex-col gap-10 bg-[#1a1e1f] rounded-full items-center p-5">
                <NuxtLink to="/">
                    <Icon name="solar:home-2-bold" size="30" class="text-white hover:text-yellow-600" />
                </NuxtLink>
                <NuxtLink to="/albums">
                    <Icon name="solar:music-library-2-bold" size="30" class="text-white hover:text-yellow-600" />
                </NuxtLink>
                <NuxtLink to="/myfav">
                    <Icon name="solar:gallery-favourite-bold" size="30" class="text-white hover:text-yellow-600" />
                </NuxtLink>
            </div>
            <div class="flex flex-col gap-10 bg-[#1a1e1f] rounded-full items-center p-5">
                <NuxtLink to="/account">
                    <Icon name="solar:user-rounded-bold" size="30" class="text-white hover:text-yellow-600" />
                </NuxtLink>
                <NuxtLink @click="null" class="cursor-pointer">
                    <Icon name="solar:login-3-bold-duotone" size="30" class="text-white hover:text-red-500" />
                </NuxtLink>
            </div>
        </div>
    </div>
</template>

<style scoped></style>