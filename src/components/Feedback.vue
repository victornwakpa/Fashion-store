<script setup>
import { ref } from 'vue';

import {Swiper, SwiperSlide} from 'swiper/vue'
// import "swiper/css"

const t = [
    {
        "id": 1,
        "name": "Emily Wilson",
        "text": "The customer experience was exceptional from start to finish. The website is user-friendly, the checkout process was smooth, and clothes I ordered fit perfectly. I'm beyond satisfied!"
    },
    {
        "id": 2,
        "name": "Sarah Thompson",
        "text": "I absolutely love the quality and style of the clothing I purchased from the website. Customer service was outstanding, and I recieved my order quickly. Highly recommended!"
    },
    {
        "id": 3,
        "name": "Olivia Martinez",
        "text": "I had a great experience shopping on this website. The cllothes I bought are fashionable and comfortable. Highly satisfied!"
    }
];

const testimonies = ref(t);
</script>

<template>
    <div class="min-h-screen grid place-content-center">
        <h2 class="text-center text-4xl font-medium text-custom-primary mb-12">Feedback Corner</h2>
        <Swiper>
            <SwiperSlide v-for="testimony in testimonies" :key="testimony.id" class="bg-green-200 odd:bg-gray-100 p-4 rounded-lg">
                <p class="text-3xl feedback-font text-custom-primary">
                    <i class="ri-chat-quote-fill"></i>
                </p>
                <h4 class="font-medium text-custom-primary text-lg my-4">{{ testimony.name }}</h4>
                <p class="text-sm leading-5">{{ testimony.text }}</p>
            </SwiperSlide>
        </Swiper>
    </div>
</template>

<style scoped>
    .swiper {
        width: 33%;
        height: 400px;
        overflow: visible;
    }
</style>