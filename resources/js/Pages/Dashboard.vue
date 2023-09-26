<script setup>
import AuthenticatedLayout from '@/Layouts/AuthenticatedLayout.vue';
import { Head } from '@inertiajs/vue3';

import 'vue3-carousel/dist/carousel.css';
import {Carousel, Navigation, Slide} from 'vue3-carousel';
</script>

<template>
    <Head title="Dashboard" />

    <AuthenticatedLayout>
        <Carousel :items-to-show="2.5" :wrap-around="true">
            <Slide v-for="slide in 10" :key="slide">
            <div class="carousel__item">{{ slide }}</div>
            </Slide>
             
            <template #addons>
            <Navigation />
            </template>
        </Carousel>
    </AuthenticatedLayout>
</template>
