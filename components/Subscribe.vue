<script setup>

</script>

<template>
    <div>
        <div class="w-full p-5 border border-yellow-600 rounded-3xl">
            <div class="flex flex-col justify-start gap-10 lg:w-1/2 mx-auto">
                <div class="flex flex-col gap-5">
                    <h6 class="text-white text-xl font-bold">
                        Subscribe to our newsletter
                    </h6>
                    <p class="text-gray-400">Subscribe to this weekly news letter so you don’t miss out on the new tech
                        topics
                        and on free code
                        snippets.</p>
                </div>
                <div class="flex justify-between items-center gap-1">
                    <UInput type="email" size="xl" variant="outline" class="w-full" color="yellow"
                        placeholder="Enter your email" />
                    <UButton color="yellow" size="xl" label="Subscribe" />
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped></style>