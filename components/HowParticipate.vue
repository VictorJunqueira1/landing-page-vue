<template>
    <div class="py-10 bg-slate-950" id="howParticipate">
        <div class="flex items-center justify-center mb-16">
            <div class="h-[1px] bg-blue-500 flex-grow"></div>
            <h2 class="text-5xl font-semibold text-white mx-4">Como Participar</h2>
            <div class="h-[1px] bg-blue-500 flex-grow"></div>
        </div>
        <div class="max-w-7xl mx-auto grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6 px-4">
            <div
                class="bg-white shadow-xl rounded-lg p-8 transition-transform transform hover:scale-105 flex flex-col items-center">
                <CameraIcon class="h-16 w-16 text-blue-600 mb-4" />
                <h3 class="text-xl font-bold text-blue-600 mb-2">1. Realize Compras</h3>
                <p class="text-gray-700 text-center">Efetue compras no valor total de R$ 500,00 ou mais para ser
                    elegível.</p>
            </div>
            <div
                class="bg-white shadow-xl rounded-lg p-8 transition-transform transform hover:scale-105 flex flex-col items-center">
                <UserIcon class="h-16 w-16 text-blue-600 mb-4" />
                <h3 class="text-xl font-bold text-blue-600 mb-2">2. Cadastro</h3>
                <p class="text-gray-700 text-center">Complete seu cadastro no nosso site, informando todos os dados
                    solicitados.</p>
            </div>
            <div
                class="bg-white shadow-xl rounded-lg p-8 transition-transform transform hover:scale-105 flex flex-col items-center">
                <TicketIcon class="h-16 w-16 text-blue-600 mb-4" />
                <h3 class="text-xl font-bold text-blue-600 mb-2">3. Receba Números da Sorte</h3>
                <p class="text-gray-700 text-center">Para cada R$ 500,00 em compras, você ganhará um número da sorte.
                </p>
            </div>
            <div
                class="bg-white shadow-xl rounded-lg p-8 transition-transform transform hover:scale-105 flex flex-col items-center">
                <CalendarIcon class="h-16 w-16 text-blue-600 mb-4" />
                <h3 class="text-xl font-bold text-blue-600 mb-2">4. Acompanhe a Apuração</h3>
                <p class="text-gray-700 text-center">A apuração será realizada no dia 04/12/2024. Fique atento aos
                    resultados!</p>
            </div>
        </div>
        <p class="mt-6 text-center text-gray-400 max-w-2xl mx-auto">
            Lembre-se: A participação é válida apenas para compras realizadas entre 18/09/2024 e 31/11/2024.
            <RegisterButton />
        </p>
    </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import { CameraIcon, UserIcon, TicketIcon, CalendarIcon } from '@heroicons/vue/24/outline';

export default defineComponent({
    name: "HowParticipate",
    components: { CameraIcon, UserIcon, TicketIcon, CalendarIcon }
});
</script>

<style scoped></style>