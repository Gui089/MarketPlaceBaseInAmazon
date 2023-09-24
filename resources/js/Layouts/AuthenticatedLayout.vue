<script setup>
import { ref } from 'vue';
import { Link } from '@inertiajs/vue3';
import MapMarkerOutline from 'vue-material-design-icons/MapMarkerOutline.vue';
import MenuDownIcon from 'vue-material-design-icons/MenuDown.vue';
import MagnifyIcon from 'vue-material-design-icons/Magnify.vue';
import CartMinusIcon from 'vue-material-design-icons/CartMinus.vue';

const showingNavigationDropdown = ref(false);
</script>

<template>
    <div class="min-w-[1150px] bg-[#fef5c8] h-full">
        <div class="flex items-center bg-[#013750] h-[60px] py-2 fixed z-50 min-w-[1150px] w-full">

            <div class="flex">
                <Link class="text-[#f23e02] h-[50px] p-2 pt-3 border-[1px] border-[#013750] rounded-sm hover:border-[1px] hover:border-[#fef5c8] cursor-pointer">
                    MARKETGUI
                </Link>
            </div>

            <div class="text-[#f23e02] h-[50px] p-2 border-[1px] border-[#013750] rounded-sm hover:border-[1px] hover:border-[#fef5c8] cursor-pointer">
                <div class="flex items center justify-center">
                    <MapMarkerOutline class="pt-2 -ml-1" fillColor="#fef5c8"/>

                    <div>
                        <div class="text-[13px] text-[#fef5c8] font-extrabold">
                            <div>Entregar para Gui</div>
                    </div>

                    <div class="text-[15px] text-[#f3dcb2] -mt-1.5 font-extrabold">
                            <div>Riacho De Santana</div>
                    </div>
                    </div>

                </div>
            </div>

            <div class="flex grow items-center h-[45px] px-1">
                <div class="flex items-center justify-center bg-[#fef5c8] border-r border-r-[#fef5c8] font-extrabold text-[11px] text-[#f23e02] w-[60px] h-[40px] rounded-l-md cursor-pointer">
                    <div class="pt-[3px]">
                        TODOS
                    </div>
                    <MenuDownIcon fillColor="#f23e02" :size="20" class="-mr-2"/>
                </div>
                <input class="block w-full border-none border-transparent focus:border-transparent focus:ring-0" type="text">
                <div class="cursor-pointer bg-[#f66b40] p-[5px] px-2 rounded-r-md">
                    <MagnifyIcon fillColor="#013750" :size="30" />
                </div>
            </div>

            <div class="flex ">
                <div class="h-[50px] p-2 border-[1px] border-[#013750] rounded-sm hover:border-[1px] hover:border-[#fef5c8] cursor-pointer">
                    <div class="flex items-center justify-center mt-2.5 px-1">
                            <img src="https://via.placeholder.com/35x20" alt="">
                            <div class="text-[15px] text-[#f3dcb2] -mt-2 -mr-0.5 font-extrabold">PT</div>
                            <MenuDownIcon fillColor="#f3dcb2" :size="20" class="-mr-4 -mt-1.5 pr-1"/>
                    </div>
                </div>

                <div class="h-[50px] p-2 border-[1px] border-[#013750] rounded-sm hover:border-[1px] hover:border-[#fef5c8] cursor-pointer">
                    <div class="flex items-center justify-center">
                        <div>
                            <div class="text-[12px] text-[#f3dcb2] font-extrabold">
                                    Olá,
                                    <span>Entrar</span>
                            </div>
                            <div class="flex items-center ">
                                <div class="text-[15px] text-[#f3dcb2] -mt-1.5  font-extrabold">Contas e Listas</div>
                                <MenuDownIcon fillColor="#f3dcb2" :size="20" class="-mr-4 -mt-1 pr-1"/>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="h-[50px] p-2 border-[1px] border-[#013750] rounded-sm hover:border-[1px] hover:border-[#fef5c8] cursor-pointer">
                    <div class="flex items-center justify-center">
                        <div>
                            <div class="text-[12px] text-[#f3dcb2] font-extrabold"> Devoluções </div>       
                            <div class="flex items-center ">
                                <div class="text-[15px] text-[#f3dcb2] -mt-1.5  font-extrabold">E Outros</div>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="relative h-[50px] p-2 border-[1px] border-[#013750] rounded-sm hover:border-[1px] hover:border-[#fef5c8] cursor-pointer">
                    <span class="absolute text-center right-[21px] w-[14px -top-0 rounded-full text-[20px]">
                        <div class="text-[#f66b40] font-extrabold bg-[#013750] h-[16px] ">0</div>
                    </span>
                    <div class="flex items-center justify-center">
                        <CartMinusIcon fillColor="#f3dcb2" :size="40" class="-mt-0.5"/>
                    </div>
                </div>
            </div>

        </div>
    </div>
</template>
