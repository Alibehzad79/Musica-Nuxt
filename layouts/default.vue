<script setup>

</script>

<template>
    <div class="mt-5">
        <Header />
        <div class="col flex lg:gap-28 mt-10 p-5">
            <div>
                <MySidebar />
            </div>
            <div class="w-full">
                <slot />
            </div>
        </div>
        <Footer />
    </div>
</template>

<style scoped></style>