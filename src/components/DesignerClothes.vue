<script setup>
    import { ref } from 'vue';
    import f from "../data/DesignerClothesData.json";

    const fashions = ref(f);
</script>

<template>
    <div class="py-16">
        <div class="text-center text-custom-primary">
            <h2 class="text-4xl md:text-5xl font-medium">Designer Clothes For You</h2>
            <p class="py-5 text-base md:text-lg">Immense yourself in the world of luxury fashion with our meeticulously crafted designer clothes!</p>
        </div>
        <div class="grid md:grid-cols-3 gap-9 place-content-center mt-8">
            <div v-for="fashion in fashions" :key="fashion.id" class="flex flex-col justify-center">
                <img :src="fashion.image" alt="">
                <div class=" text-center">
                    <div class="flex justify-center items-center flex-col py-8">
                        <p class="pb-1 font-bold text-2xl">{{ fashion.title }}</p>
                        <p class="flex justify-between gap-4">
                            {{ fashion.desc }}
                        </p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>