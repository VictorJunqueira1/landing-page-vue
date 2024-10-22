<template>
    <nav class="bg-slate-950 text-white px-4 py-2 flex items-center justify-between">
        <!-- (Desktop) -->
        <div class="hidden lg:block w-full">
            <div class="flex items-center mx-auto max-w-7xl py-4">
                <div class="rounded-lg flex items-center justify-center mr-4 p-2">
                    <img src="https://www.zarla.com/images/zarla-bratecno-1x1-2400x2400-20210604-dxh9rm88pqf67dy3gcwr.png?crop=1:1,smart&width=250&dpr=2"
                        alt="BRATECNO" class="h-28" />
                </div>
                <ul class="flex gap-6 text-lg justify-center flex-1">
                    <li><a href="#home"
                            class="hover:text-blue-600 transition-all ease-in-out duration-300 text-white">HOME</a></li>
                    <li><a href="#howParticipate" class="hover:text-blue-600 transition-all ease-in-out duration-300 text-white">COMO
                            PARTICIPAR</a></li>
                    <li><a href="#prizes"
                            class="hover:text-blue-600 transition-all ease-in-out duration-300 text-white">PRÊMIOS</a>
                    </li>
                    <li><a href="#faq"
                            class="hover:text-blue-600 transition-all ease-in-out duration-300 text-white">DÚVIDAS
                            FREQUENTES</a></li>
                    <li><a href="#winners"
                            class="hover:text-blue-600 transition-all ease-in-out duration-300 text-white">GANHADORES</a>
                    </li>
                </ul>
                <div class="flex items-center space-x-2">
                    <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24"
                        stroke="currentColor" stroke-width="2">
                        <path stroke-linecap="round" stroke-linejoin="round"
                            d="M12 14c4.418 0 8 3.582 8 8v2H4v-2c0-4.418 3.582-8 8-8zM12 12a4 4 0 100-8 4 4 0 000 8z" />
                    </svg>
                    <a href="#"
                        class="hover:text-blue-600 transition-all ease-in-out duration-300 text-white font-semibold">LOGIN/CADASTRAR</a>
                </div>
            </div>
        </div>

        <!-- (Mobile) -->
        <div class="block lg:hidden w-full py-4">
            <Sheet>
                <SheetTrigger as-child>
                    <button class="flex items-center justify-between w-full">
                        <div class="flex items-center justify-center mr-4 px-6 py-3">
                            <span class="text-white font-semibold text-2xl">BRATECNO</span>
                        </div>
                        <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8" fill="none" viewBox="0 0 24 24"
                            stroke="currentColor" stroke-width="2">
                            <path stroke-linecap="round" stroke-linejoin="round" d="M4 6h16M4 12h16m-7 6h7" />
                        </svg>
                    </button>
                </SheetTrigger>
                <SheetContent>
                    <SheetHeader>
                        <SheetTitle class="text-left pl-3">BRATECNO</SheetTitle>
                    </SheetHeader>
                    <div class="border-b border-gray-400 mt-2"></div>
                    <ul class="flex flex-col gap-4 px-4 py-4 space-y-4 text-lg font-semibold">
                        <li><a href="#home"
                                class="hover:text-blue-600 transition-all ease-in-out duration-300 text-black">HOME</a>
                        </li>
                        <li><a href="#howParticipate"
                                class="hover:text-blue-600 transition-all ease-in-out duration-300 text-black">COMO
                                PARTICIPAR</a></li>
                        <li><a href="#prizes"
                                class="hover:text-blue-600 transition-all ease-in-out duration-300 text-black">PRÊMIOS</a>
                        </li>
                        <li><a href="#faq"
                                class="hover:text-blue-600 transition-all ease-in-out duration-300 text-black">DÚVIDAS
                                FREQUENTES</a></li>
                        <li><a href="#winners"
                                class="hover:text-blue-600 transition-all ease-in-out duration-300 text-black">GANHADORES</a>
                        </li>
                        <div class="flex items-center space-x-2">
                            <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24"
                                stroke="currentColor" stroke-width="2">
                                <path stroke-linecap="round" stroke-linejoin="round"
                                    d="M12 14c4.418 0 8 3.582 8 8v2H4v-2c0-4.418 3.582-8 8-8zM12 12a4 4 0 100-8 4 4 0 000 8z" />
                            </svg>
                            <a href="#login"
                                class="hover:text-blue-600 transition-all ease-in-out duration-300 text-black font-semibold">LOGIN/CADASTRAR</a>
                        </div>
                    </ul>
                </SheetContent>
            </Sheet>
        </div>
    </nav>
</template>

<script setup lang="ts">
import {
    Sheet,
    SheetContent,
    SheetHeader,
    SheetTitle,
    SheetTrigger,
} from '@/components/ui/sheet'
</script>

<style scoped></style>