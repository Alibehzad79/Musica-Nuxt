<script setup>

</script>

<template>
    <div>
        <div class="container mx-auto flex flex-col gap-20 mb-10">
            <div class="w-full relative">
                <img src="https://imageupscaler.com/wp-content/uploads/2024/07/maple-leaf-enlarged.jpg" alt="image"
                    class="w-full h-40 lg:h-96 rounded-3xl">
                <div class="absolute -bottom-20 left-5 rounded-full">
                    <img src="https://letsenhance.io/static/03620c83508fc72c6d2b218c7e304ba5/11499/UpscalerAfter.jpg"
                        alt="image" class="w-[8rem] lg:w-[13rem] h-[8rem] lg:h-[13rem] rounded-full">
                </div>
            </div>
            <div class="w-full lg:w-1/2 mx-auto mt-10">
                <form action="#" method="post" class="flex flex-col gap-5">
                    <div class="flex flex-col lg:flex-row lg:justify-between items-center gap-3">
                        <UInput type="text" placeholder="First Name" size="xl" class="w-full border border-gray-600 rounded-xl text-white" variant="none" />
                        <UInput type="text" placeholder="Last Name" size="xl" class="w-full border border-gray-600 rounded-xl text-white" variant="none" />
                    </div>
                    <UInput type="text" placeholder="Username" size="xl" variant="none" class="w-full border border-gray-600 rounded-xl text-white" />
                    <UInput type="email" placeholder="email@mail.com" size="xl" variant="none" class="w-full border border-gray-600 rounded-xl text-white" />
                    <UButton label="Save" size="xl" color="orange" class="justify-center" />
                </form>
            </div>
        </div>
    </div>
</template>