<script setup>
    import {ref} from 'vue';
    import OurProductsData from '../data/OurProductsData.json'

    const ProductItems = ref(OurProductsData);
</script>

<template>
    <div class=" min-h-screen">
        <div class="text-custom-primary text-center">
            <h2 class="text-4xl md:text-5xl font-medium my-5">Our Products</h2>
            <div class="grid grid-cols-2 font-medium my-10 text-lg">
                <a href="#" class="mx-5 px-3 bg-slate-50 my-2">SALE</a>
                <a href="#" class="mx-5 px-3 bg-slate-50 my-2">HOT</a>
                <a href="#" class="mx-5 px-3 bg-slate-50 my-2">NEW ARRIVALS</a>
                <a href="#" class="mx-5 px-3 bg-slate-50 my-2">ACCESSORIES</a>
            </div>
        </div>

        <div class="grid grid-cols-2 md:grid-cols-4 gap-6 place-content-center mt-8">
            <div v-for="item in ProductItems" :key="item.id" class="flex flex-col">
                <img :src="item.image" class="text-center" alt="">
                <div class=" text-center">
                    <div class="flex justify-center items-center flex-col py-8">
                        <p class="pb-1 font-bold">{{ item.name }}</p>
                        <p class="flex justify-between gap-4">
                            <span>${{ item.price }}</span>
                            <span> | </span>
                            <span class="flex">
                            {{ item.rating }}
                            <img :src="item.icon" class="pl-2" alt="">
                            </span>
                        </p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>