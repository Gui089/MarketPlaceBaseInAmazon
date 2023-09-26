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

        <main>
            <div class="pt-[98px]"></div>
            <slot />
        </main>

        <div class="w-full bg-[#f3dcb2] mt-10">
            <div class="max-w-[1500px] mx-auto">
                    <div class="text-[23px] pt-4 font-extrabold">Recomendado com base em suas tendências de compras</div>
                    <div class="flex justify-center items-stretch">
                        <div class="pt-4 text-center mx-auto">
                            <div class="w-[158px] h-[150px] overflow-hidden">
                                <img src="https://via.placeholder.com/158x150" alt="">
                            </div>
                            <div class="w-[160px] text-[12px] py-2 text-teal-600 font-extrabold hover:text-red-600 cursor-pointer">
                                Este um título de teste
                            </div>
                            <div class="flex justify-start">
                                <div class="text-xs font-extrabold text-red-600 w-full text-left">R$%500.00</div>
                            </div>
                        </div>
                    </div>
            </div>
        </div>

        <footer class="bg-[#013750]">
            <div class="bg-[#2c6b74] hover:bg-[#00988d] w-full p-3.5 cursor-pointer text-[#fef5c8] font-extrabold text-center">
                    Voltar ao topo
            </div>
            <div class="flex items-stretch justify-between max-w-[1000px] mx-auto p-10 text-[#fef5c8]">
                    <ul>
                        <li class="font-extrabold text-lg">Conheça-nos</li>
                        <li class="hover:underline cursor-pointer">Meu linkedin</li>
                        <li class="hover:underline cursor-pointer">Sobre MarketGui</li>
                        <li class="hover:underline cursor-pointer">Quem sou eu</li>
                        <li class="hover:underline cursor-pointer">Minhas habilidades</li>
                        <li class="hover:underline cursor-pointer">GitHub</li>
                    </ul>

                    <ul>
                        <li class="font-extrabold text-lg">Faça dinheiro com a gente</li>
                        <li class="hover:underline cursor-pointer">Como posso te ajudar ?</li>
                        <li class="hover:underline cursor-pointer">adquira meus serviços</li>
                        <li class="hover:underline cursor-pointer">Peça o seu orcamento</li>
                        <li class="hover:underline cursor-pointer">Alavanque os seus negócios</li>
                        <li class="hover:underline cursor-pointer">Contrate-me</li>
                        <li class="hover:underline cursor-pointer">Adquira outros projetos</li>
                    </ul>

                    <ul>
                        <li class="font-extrabold text-lg">Conheça-nos</li>
                        <li class="hover:underline cursor-pointer">Meu linkedin</li>
                        <li class="hover:underline cursor-pointer">Sobre MarketGui</li>
                        <li class="hover:underline cursor-pointer">Quem sou eu</li>
                        <li class="hover:underline cursor-pointer">Minhas habilidades</li>
                        <li class="hover:underline cursor-pointer">GitHub</li>
                    </ul>

                    <ul>
                        <li class="font-extrabold text-lg">Faça dinheiro com a gente</li>
                        <li class="hover:underline cursor-pointer">Como posso te ajudar ?</li>
                        <li class="hover:underline cursor-pointer">adquira meus serviços</li>
                        <li class="hover:underline cursor-pointer">Peça o seu orcamento</li>
                        <li class="hover:underline cursor-pointer">Alavanque os seus negócios</li>
                        <li class="hover:underline cursor-pointer">Contrate-me</li>
                        <li class="hover:underline cursor-pointer">Adquira outros projetos</li>
                    </ul>
            </div>
        </footer>
    </div>
</template>
