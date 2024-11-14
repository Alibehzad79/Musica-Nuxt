<script setup>

const searchValue = ref()
const openMenu = ref(false)

const getLogOut = async()=> {
    openMenu.value = false
    await navigateTo('/')
}

const goSearch = async () => {
    await navigateTo('/albums')
}

</script>

<template>
    <div class="sticky top-0 w-full z-50 bg-cover backdrop-blur-md p-2 lg:p-5 rounded-b-3xl">
        <div class="flex items-center gap-10 justify-between">
            <Icon name="solar:music-notes-bold-duotone" size="50" class="text-white" />
            <UInput placeholder="Search" v-model="searchValue" icon="solar:magnifer-outline"
                class="w-full text-white hidden lg:flex bg-gray-700 rounded-3xl" size="xl" variant="none"
                v-on:keyup.enter="goSearch">
                <template #trailing v-if="searchValue">
                    <UKbd value="Enter" />
                </template>
            </UInput>
            <UButton icon="solar:hamburger-menu-broken" @click="openMenu = true" size="xl" color="white" variant="solid"
                class="lg:hidden" />
            <USlideover v-model="openMenu" class="lg:hidden">
                <UCard class="flex flex-col flex-1"
                    :ui="{ body: { base: 'flex-1' }, ring: '', divide: 'divide-y divide-none', background: 'bg-[#1a1e1f]' }">
                    <template #header>
                        <UButton color="red" variant="ghost" size="sm" icon="i-heroicons-x-mark-20-solid"
                            class="flex lg:hidden absolute end-5 top-5 z-10" square padded @click="openMenu = false" />
                    </template>
                    <UInput placeholder="Search" v-model="searchValue" icon="solar:magnifer-outline"
                        class="w-full text-white mb-5 bg-gray-700 rounded-3xl" size="xl" variant="none"
                        v-on:keyup.enter="goSearch">
                        <template #trailing v-if="searchValue">
                            <UKbd value="Enter" />
                        </template>
                    </UInput>
                    <div class="flex flex-col">
                        <div class="flex flex-col gap-10 p-5">
                            <NuxtLink @click="openMenu = false" to="/" class="flex items-center gap-5">
                                <Icon name="solar:home-2-bold" size="30" class="text-white hover:text-yellow-600" />
                                <span class="text-white">Home</span>
                            </NuxtLink>
                            <NuxtLink @click="openMenu = false" to="/albums" class="flex items-center gap-5">
                                <Icon name="solar:music-library-2-bold" size="30"
                                    class="text-white hover:text-yellow-600" />
                                <span class="text-white">Albums</span>
                            </NuxtLink>
                            <NuxtLink @click="openMenu = false" to="/myfav" class="flex items-center gap-5">
                                <Icon name="solar:gallery-favourite-bold" size="30"
                                    class="text-white hover:text-yellow-600" />
                                <span class="text-white">May Fav</span>
                            </NuxtLink>
                            <NuxtLink @click="openMenu = false" to="/account" class="flex items-center gap-5">
                                <Icon name="solar:user-rounded-bold" size="30"
                                    class="text-white hover:text-yellow-600" />
                                <span class="text-white">Account</span>
                            </NuxtLink>
                            <NuxtLink @click="getLogOut" class="cursor-pointer flex items-center gap-5">
                                <Icon name="solar:login-3-bold-duotone" size="30" class="text-red-500" />
                                <span class="text-red-500">Logout</span>
                            </NuxtLink>
                        </div>
                    </div>
                </UCard>
            </USlideover>
        </div>
    </div>
</template>

<style scoped></style>