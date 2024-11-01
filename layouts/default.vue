<script setup>

</script>

<template>
    <div class="mt-5 mx-5">
        <Header />
        <div class="col flex lg:gap-28 mt-10">
            <div>
                <MySidebar />
            </div>
            <div class="w-full">
                <slot />
            </div>
        </div>
    </div>
</template>

<style scoped></style>