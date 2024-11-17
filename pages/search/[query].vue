<script setup>
const route = useRoute()
const query = route.params.query

const datas = [
    {
        id: 1,
        title: 'Sekerim',
        description: "2009 popular music",
        singer: "Ismail YK"
    },
    {
        id: 2,
        title: 'Ask',
        description: "2015 popular music",
        singer: "Irem"
    },
    {
        id: 3,
        title: 'Dost',
        description: "2023 popular music",
        singer: "Ibrahim Tatlises"
    },
]

</script>

<template>
    <div>
        <div class="flex flex-col gap-3 mb-10">
            <SearchResultCard v-for="data in datas" :key="data.id" :title="data.title" :description="data.description"
                :singer="data.singer" />
        </div>
    </div>
</template>

<style scoped></style>