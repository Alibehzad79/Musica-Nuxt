<script setup>
import { useTemplateRef } from 'vue'
import { useMediaControls } from '@vueuse/core'
const props = defineProps([
    "src",
    'image',
    'title',
    'subtitle'
])
const loop = ref(false)
const range = ref(0)
const volume = ref(60)
const played = ref(false)
const paused = ref(false)
const mute = ref(false)

const player = useTemplateRef('player')

const play = () => {
    paused.value = false
    played.value = true
    player.value.play()
}
const pause = () => {
    played.value = false
    paused.value = true
    player.value.pause()
}

const muted = () => {
    if (player.value.volume == 0) {
        mute.value = false
        volume.value = 100
        player.value.volume = 1
    } else {
        mute.value = true
        volume.value = 0
        player.value.volume = 0
    }
}
const time_convert = (num) => {
    var hours = Math.floor(num / 60);
    var minutes = num % 60;
    if (hours < 10) {
        hours = '0' + hours
    }
    if (minutes < 10) {
        minutes = '0' + minutes
    }
    return hours + ":" + minutes;
}
</script>

<template>
    <div>
        <audio v-on:timeupdate="range = player?.currentTime" ref="player" :loop="loop" class="bg-gray-600 rounded-3xl">
            <source :src="src" type="audio/mp3">
        </audio>
    </div>
    <div class="rounded-3xl shadow-2xl">
        <div class="flex flex-col lg:flex-row justify-between p-5 gap-5 lg:gap-10 items-start rounded-3xl">
            <div class="flex items-center gap-5 w-1/2">
                <img :src="image" :alt="title" :title="title" class="hidden lg:flex w-[5rem] h-[5rem] rounded-xl" />
                <div class="flex flex-col lg:gap-5 justify-between">
                    <strong class="text-white">{{ title }}</strong>
                    <span class="text-gray-400">{{ subtitle }}</span>
                </div>
            </div>
            <div class="flex flex-col gap-5 justify-between w-full">
                <div class="flex items-center gap-10 mx-auto">
                    <span class="text-white">{{ time_convert(Math.floor(range)) }}</span>
                    <UIcon name="solar:play-line-duotone" size="35" class="cursor-pointer text-white"
                        :class="{ 'text-yellow-400': played, 'text-white': !played }" @click="play" />
                    <UIcon name="solar:pause-line-duotone" size="35" class="cursor-pointer text-white"
                        :class="{ 'text-yellow-400': paused, 'text-white': !paused }" @click="pause" />
                    <UIcon name="solar:repeat-one-bold" size="35" class="cursor-pointer text-white"
                        :class="{ 'text-yellow-400': loop, 'text-white': !loop }" @click="loop = !loop" />
                    <span class="text-white">{{ time_convert(Math.floor(player?.duration)) }}</span>
                </div>
                <URange v-model="range" :min="0" v-on:update:model-value="player.currentTime = range"
                    :max="player?.duration" color="yellow" size="sm" />
            </div>
            <div class="w-full lg:w-1/2 flex flex-row lg:flex-col items-center justify-center gap-5">
                <div class="flex items-center gap-2 w-1/2">
                    <UIcon name="solar:muted-bold" size="35" class="cursor-pointer text-white"
                        :class="{ 'text-yellow-400': mute, 'text-white': !mute }" @click="muted" />
                    <URange v-model="volume" v-on:update:model-value="player.volume = volume / 100" :min="0" :max="100"
                        color="yellow" size="sm" />
                </div>
                <a :href="src" download
                    class="text-yellow-400 flex items-center gap-2 text-sm border border-yellow-400 p-1 rounded lg:w-1/2 justify-center">
                    <Icon name="solar:download-square-bold" /> Download
                </a>
            </div>
        </div>
    </div>
</template>

<style scoped></style>