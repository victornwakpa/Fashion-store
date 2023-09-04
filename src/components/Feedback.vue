<script setup>
import { ref } from 'vue';

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
        <div class="grid grid-cols-3 gap-10">
            <div v-for="testimony in testimonies" :key="testimony.id" class="bg-green-200 p-4 rounded-lg">
                <p></p>
                <h4 class="font-medium text-custom-primary text-lg my-4">{{ testimony.name }}</h4>
                <p class="text-sm leading-5">{{ testimony.text }}</p>
            </div>
        </div>
    </div>
</template>