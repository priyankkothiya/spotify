<script setup>
    import CategorySelect from '../components/CategorySelect.vue';
    import { ref } from 'vue';
    const browsesAll = ref([
    {
        label: 'Music',
        icon: '/src/assets/cat-1.jpeg',
    },
    {
        label: 'PodCast',
        icon: '/src/assets/cat-4.jpeg',
    },
    {
        label: 'Live Event',
        icon: '/src/assets/cat-3.jpg',
    },
    {
        label: '2024 in Music',
        icon: '/src/assets/cat-2.jpeg',
    },
    {
        label: '2024 in Podacast',
        icon: '/src/assets/cat-1.jpeg',
    },
    {
        label: 'Mase For You',
        icon: '/src/assets/cat-3.jpg',
    },
    {
        label: 'New Releases',
        icon: '/src/assets/cat-2.jpeg',
    },
    {
        label: 'Hindi',
        icon: '/src/assets/cat-4.jpeg',
    },
    {
        label: 'Punjabi',
        icon: '/src/assets/cat-2.jpeg',
    },
    {
        label: 'Tamil',
        icon: '/src/assets/cat-1.jpeg',
    },
    {
        label: 'Telugu',
        icon: '/src/assets/cat-3.jpg',
    },
    {
        label: 'Podcat Charts',
        icon: '/src/assets/cat-1.jpeg',
    },
    {
        label: 'Malyalam',
        icon: '/src/assets/cat-4.jpeg',
    },
    {
        label: 'Bhojpuri',
        icon: '/src/assets/cat-1.jpeg',
    },
    {
        label: 'Happy Holidays',
        icon: '/src/assets/cat-2.jpeg',
    },
    {
        label: 'Summer',
        icon: '/src/assets/cat-3.jpg',
    },
    {
        label: 'Discover',
        icon: '/src/assets/cat-1.jpeg',
    },
    {
        label: 'Malyalam',
        icon: '/src/assets/cat-2.jpeg',
    },
    {
        label: 'Bhojpuri',
        icon: '/src/assets/cat-3.jpg',
    },
    {
        label: 'Happy Holidays',
        icon: '/src/assets/cat-4.jpeg',
    },
    ]);
</script>

<template>
    <div class="p-8">
        <button
            type="button"
            class="text-white text-2xl font-semibold hover:underline cursor-pointer"
        >
            Browse all
        </button>

        <div class="py-1.5"></div>

        <div class="grid xl:grid-cols-4 lg:grid-cols-4 md:grid-cols-3 sm:grid-cols-2 gap-6">
            <CategorySelect v-for="(browse, index) in browsesAll" :key="index" :category="browse.label" :image="browse.icon"/>
        </div>
    </div>
</template>
