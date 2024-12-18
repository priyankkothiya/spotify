<script setup>
    import HomeCard from '../components/HomeCard.vue';
    import { ref } from 'vue';
    const singerAll = ref([
    {
        name: 'Pritam',
        icon: '/src/assets/singer-1.jpeg',
    },
    {
        name: 'Sachin-Jigar',
        icon: '/src/assets/singer-2.jpeg',
    },
    {
        name: 'A.R. Rahman',
        icon: '/src/assets/singer-3.jpeg',
    },
    {
        name: 'Arijit Singh',
        icon: '/src/assets/singer-4.jpeg',
    },
    {
        name: 'Vishal-Shekhar',
        icon: '/src/assets/singer-5.jpeg',
    },
    {
        name: 'Atif Aslam',
        icon: '/src/assets/singer-6.jpeg',
    },
    ]);
    const albumsAll = ref([
    {
        name: 'Glory',
        title: 'Yo Yo Honey Singh',
        icon: '/src/assets/a1.jpeg',
    },
    {
        name: 'Patandar',
        title: 'Arjan Dhillon maxi',
        icon: '/src/assets/a2.jpeg',
    },
    {
        name: 'Aashiqui2',
        title: 'Mithoon, ankit tiwari',
        icon: '/src/assets/a3.jpeg',
    },
    {
        name: 'Jo Tum Mere Ho',
        title: 'Anuv Jain',
        icon: '/src/assets/a4.jpeg',
    },
    {
        name: 'Making Memories',
        title: 'karan AAujla, iikay',
        icon: '/src/assets/a5.jpeg',
    },
    {
        name: 'Yeh Jawaani',
        title: 'Pritam',
        icon: '/src/assets/a6.jpeg',
    },
    ])
    const popularAll = ref([
    {
        name: 'Arjit Singh',
        title: 'With You Sachin jigar, Pritam, Vishal Shekhar',
        icon: '/src/assets/1.jpeg',
    },
    {
        name: 'Diljit Dosanjh',
        title: 'With You Sachin jigar, Pritam, Vishal Shekhar',
        icon: '/src/assets/2.jpeg',
    },
    {
        name: 'Udit Narayan',
        title: 'With You Sachin jigar, Pritam, Vishal Shekhar',
        icon: '/src/assets/3.jpeg',
    },
    {
        name: 'KK',
        title: 'With You Sachin jigar, Pritam, Vishal Shekhar',
        icon: '/src/assets/4.jpeg',
    },
    {
        name: 'Shreya  Ghoshal',
        title: 'With You Sachin jigar, Pritam, Vishal Shekhar',
        icon: '/src/assets/5.jpeg',
    },
    {
        name: 'Sidhu Moose Wala',
        title: 'Pritam',
        icon: '/src/assets/6.jpeg',
    },
    ])
    const featureAll = ref([
    {
        name: 'Arjit Singh',
        title: 'Your weekly update of the most played tracks right now - Global.',
        icon: '/src/assets/f1.jpg',
    },
    {
        name: 'Diljit Dosanjh',
        title: 'Your weekly update of the most played tracks right now - Global.',
        icon: '/src/assets/f2.jpg',
    },
    {
        name: 'Udit Narayan',
        title: 'Your weekly update of the most played tracks right now - Global.',
        icon: '/src/assets/f3.jpg',
    },
    {
        name: 'KK',
        title: 'Your weekly update of the most played tracks right now - Global.',
        icon: '/src/assets/f4.jpg',
    },
    {
        name: 'Shreya  Ghoshal',
        title: 'Your weekly update of the most played tracks right now - Global.',
        icon: '/src/assets/f5.jpg',
    },
    {
        name: 'Sidhu Moose Wala',
        title: 'Your weekly update of the most played tracks right now - Global.',
        icon: '/src/assets/f6.jpg',
    },
    ])
    const wrappedAll = ref([
    {
        name: 'Arjit Singh',
        title: 'The most streamed songs of 2024. Cover: Sabrina Carpenter',
        icon: '/src/assets/2024-1.jpeg',
    },
    {
        name: 'Diljit Dosanjh',
        title: 'Editor`s most streamed songs of 2024. Cover: Sabrina Carpenter',
        icon: '/src/assets/2024-2.jpeg',
    },
    {
        name: 'Udit Narayan',
        title: 'Editor`s most streamed songs of 2024. Cover: Sabrina Carpenter',
        icon: '/src/assets/2024-3.jpeg',
    },
    {
        name: 'KK',
        title: 'The most streamed songs of 2024. Cover: Sabrina Carpenter',
        icon: '/src/assets/2024-4.jpeg',
    },
    {
        name: 'Shreya  Ghoshal',
        title: 'The most streamed songs of 2024. Cover: Sabrina Carpenter',
        icon: '/src/assets/2024-5.jpeg',
    },
    {
        name: 'Sidhu Moose Wala',
        title: 'Our Editor`s streamed songs of 2024. Cover: Sabrina Carpenter',
        icon: '/src/assets/2024-6.jpeg',
    },
    ])
</script>

<template>
    <div class="p-5">
        <button
            type="button"
            class="text-white text-2xl font-semibold hover:underline cursor-pointer"
        >
            Popular artists
        </button>
        <div class="py-1.5"></div>
        <div class="flex items-center">
            <HomeCard class="rounded-full" v-for="singer in singerAll" :key="singer.name" custome="rounded-full" :image="singer.icon" :title="singer.name" subTitle="Artist" />
        </div>
    </div>
    <div class="p-5">
        <button
            type="button"
            class="text-white text-2xl font-semibold hover:underline cursor-pointer"
        >
        Popular albums and singles
        </button>
        <div class="py-1.5"></div>
        <div class="flex items-center">
            <HomeCard v-for="album in albumsAll" :key="album.name" :image="album.icon" :title="album.name" :subTitle="album.title" />
        </div>
    </div>
    <div class="p-5">
        <button
            type="button"
            class="text-white text-2xl font-semibold hover:underline cursor-pointer"
        >
        Popular radio
        </button>
        <div class="py-1.5"></div>
        <div class="flex items-center">
            <HomeCard v-for="popular in popularAll" :key="popular.name" :image="popular.icon" :subTitle="popular.title" />
        </div>
    </div>
    <div class="p-5">
        <button
            type="button"
            class="text-white text-2xl font-semibold hover:underline cursor-pointer"
        >
        Featured Charts
        </button>
        <div class="py-1.5"></div>
        <div class="flex items-center">
            <HomeCard v-for="feature in featureAll" :key="feature.name" :image="feature.icon" :subTitle="feature.title" />
        </div>
    </div>
    <div class="p-5">
        <button
            type="button"
            class="text-white text-2xl font-semibold hover:underline cursor-pointer"
        >
        2024 Wrapped
        </button>
        <div class="py-1.5"></div>
        <div class="flex items-center">
            <HomeCard v-for="wrapped in wrappedAll" :key="wrapped.name" :image="wrapped.icon" :subTitle="wrapped.title" />
        </div>
    </div>
</template>
