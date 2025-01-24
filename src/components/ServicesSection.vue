<template >
    <section class="text-white mt-20" id="services">
        <div class="px-4 xl:pl-16">
            <h2 class="text-4xl font-bold text-white mb-4">My Services</h2>
        </div>
        <div class="py-8 xl:px-16 px-4 sm:py-16 grid grid-cols-1 gap-6 pt-10 sm:grid-cols-2 md:gap-10 md:pt-12 lg:grid-cols-3">
            <div v-for="service in services" :key="service.id" data-aos="fade-up"
            class="px-8 py-12 rounded-xl bg-[#111a3e] shadow-lg border border-[#1f1641]"
            >
                <div class="mx-auto h-24 w-24 text-center xl:h-28 xl:w-28">
                    <div>
                        <img :src="service.icon" alt="service icon">
                    </div>
                </div>
                <div class="text-center">
                    <h3 class="pt-8 text-lg font-semibold uppercase text-transparent bg-clip-text bg-gradient-to-r from-primary to-secondary lg:text-xl">
                        {{ service.name }}
                    </h3>
                    <p class="text-grey pt-4 text-sm group-hover:text-white md:text-base">
                        {{ service.description }}
                    </p>
                </div>
            </div>
        </div>
    </section>
</template>
<script setup>
import {ref} from 'vue';
const services = ref([
    {
        id: 1,
        icon: "https://img.icons8.com/ios-filled/100/ffffff/google-code.png",
        name: "Web Development",
        description: "Crafting responsive and user-friendly websites tailored to your business needs.",
    },
    {
        id: 2,
        icon: "https://img.icons8.com/?size=100&id=gu6xC0FPd85M&format=png&color=000000",
        name: "CAD Design",
        description: "Designing precise and detailed 2D and 3D models for engineering and architecture projects.",
    },
    {
        id: 3,
        icon: "https://img.icons8.com/?size=100&id=p2YCDur26Xn9&format=png&color=000000",
        name: "Structural Analysis",
        description: "Performing comprehensive structural analysis to ensure safety and efficiency of designs.",
    },
    {
        id: 4,
        icon: "https://img.icons8.com/?size=100&id=Lg1DdV2aXCLu&format=png&color=000000",
        name: "Quality Analysis",
        description: "Ensuring the highest standards of quality through meticulous testing and validation.",
    },
]);
</script>

