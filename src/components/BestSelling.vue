<script setup>
    import { ref } from 'vue';
    import f from "../data/data.json";

    const fashions = ref(f);
</script>

<template>
    <div class="py-16">
        <div class="text-center text-custom-primary">
            <h2 class="text-5xl font-medium">Best Selling</h2>
            <p class="py-5 text-lg">Get in on the trend with our curated selection of bet-selling styles.</p>
        </div>
        <div class="grid grid-cols-3 place-content-center mt-8">
            <div v-for="fashion in fashions" :key="fashion.id" class="grid place-content-center">
                <img :src="fashion.image" class="h-96 text-center" alt="">
                <div class=" text-center">
                    <div class="flex justify-center items-center flex-col py-8">
                        <p class="pb-1 font-bold">{{ fashion.name }}</p>
                        <p class="flex justify-between gap-4">
                            <span>${{ fashion.price }}</span>
                            <span> | </span>
                            <span class="flex">
                            {{ fashion.rating }}
                            <img :src="fashion.icon" class="pl-2" alt="">
                            </span>
                        </p>
                    </div>
                </div>
            </div>
        </div>
        <div class="text-center my-4">
            <button class="btn btn-outline rounded-none px-8 border-[#224F34] border-2">
            See all
                <span class="inline-block">
                    <i class="ri-arrow-right-line"></i>
                </span>
            </button>
        </div>
        
    </div>
</template>