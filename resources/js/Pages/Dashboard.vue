<script setup>
import AuthenticatedLayout from '@/Layouts/AuthenticatedLayout.vue';
import { Head } from '@inertiajs/vue3';

import 'vue3-carousel/dist/carousel.css';
import {Carousel, Navigation, Slide} from 'vue3-carousel';
</script>

<template>
    <Head title="Dashboard" />

    <AuthenticatedLayout>
        <Carousel :items-to-show="1" :wrap-around="true">
            <Slide v-for="slide in 10" :key="slide">
            <div class="carousel__item">
                <img src="https://via.placeholder.com/3000x1200.png/004466?text=Testing" alt="">
            </div>
            </Slide>
             
            <template #addons>
            <Navigation />
            </template>
        </Carousel>

        <div class="relative -mt-[300px]">
            <div class="flex m-4 z-10 relative">
                <div class="bg-[#fef5c8] mx-2 p-2 text-md w-full text-center">
                    Você está no MarketGui.com aqui você compra o que quiser e onde quiser e com a melhor qualidade do mercado.
                    <span class="underline text-teal-600 cursor-pointer">Clique aqui para ir ao meu Portifólio</span>
                </div>
            </div>

            <div class="grid grid-cols-3 m-4 z-10 relative">
                <div class="p-1.5 flex">
                    <div class="bg-[#fef5c8] p-5">
                        <div class="text-2xl font-extrabold flex">Computadores</div>
                        <div class="flex">
                            <img class="object-fill" src="https://via.placeholder.com/1097x756" alt="">
                        </div>
                        <div class="pt-3 -mb-2 text-teal-800 font-bold hover:underline hover:text-red-400 cursor-pointer">
                            Saiba mais
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </AuthenticatedLayout>
</template>

<style>
.carousel__item{
    font-size: 20px;
    display: flex;
    justify-content: center;
    align-items: center;
}

.carousel__prev,
.carousel__next{
    width: 40px;
    height: 200px;
    color: #f9f4e1;
    margin-top: -100px;
    border: transparent;
}
.carousel__prev:hover,
.carousel__next:hover {
    width: 40px;
    height: 200px;
    color:#fef5c8 ;
    margin-top: -100px;
    border: 3px solid #e8df9c ;
}

</style>
