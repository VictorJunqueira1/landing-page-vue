<template>
  <div
    class="p-6 border-t border-gray-800 shadow-md text-white mx-auto max-w-7xl h-full mb-32 flex items-center justify-center flex-col"
    id="winners">
    <h1
      class="text-4xl font-bold mt-24 mb-12 text-center bg-gradient-to-r from-blue-500 to-indigo-700 bg-clip-text text-transparent">
      GANHADORES
    </h1>
    <Accordion type="single" collapsible class="w-full">
      <AccordionItem class="mb-4" value="sorteio-1">
        <AccordionTrigger
          class="flex justify-between items-center font-semibold border border-gray-800 mb-2 rounded-lg bg-slate-900 text-xl text-muted-foreground cursor-pointer transition duration-200 ease-in-out">
          <span class="px-4">1º SORTEIO 05/01/2024</span>
        </AccordionTrigger>
        <AccordionContent class="bg-slate-800 rounded-md p-4">
          <div v-for="(winner, index) in winners1" :key="index" class="border-b border-muted mb-2 pb-2">
            <p class="font-bold">Nome: {{ winner.name }}</p>
            <p class="text-muted">CPF: {{ winner.cpf }}</p>
            <p class="text-muted">Número da sorte: {{ winner.luckyNumber }}</p>
            <p class="text-muted">Prêmio: {{ winner.prize }}</p>
          </div>
        </AccordionContent>
      </AccordionItem>

      <AccordionItem class="mb-4" value="sorteio-2">
        <AccordionTrigger
          class="flex justify-between items-center font-semibold border border-gray-800 mb-2 rounded-lg bg-slate-900 text-xl text-muted-foreground cursor-pointer transition duration-200 ease-in-out">
          <span class="px-4">2º SORTEIO 15/02/2024</span>
        </AccordionTrigger>
        <AccordionContent class="bg-slate-800 rounded-md p-4">
          <div v-for="(winner, index) in winners2" :key="index" class="border-b border-muted mb-2 pb-2">
            <p class="font-bold">Nome: {{ winner.name }}</p>
            <p class="text-muted">CPF: {{ winner.cpf }}</p>
            <p class="text-muted">Número da sorte: {{ winner.luckyNumber }}</p>
            <p class="text-muted">Prêmio: {{ winner.prize }}</p>
          </div>
        </AccordionContent>
      </AccordionItem>

      <AccordionItem class="mb-4" value="sorteio-3">
        <AccordionTrigger
          class="flex justify-between items-center font-semibold border border-gray-800 mb-2 rounded-lg bg-slate-900 text-xl text-muted-foreground cursor-pointer transition duration-200 ease-in-out">
          <span class="px-4">3º SORTEIO 25/03/2024</span>
        </AccordionTrigger>
        <AccordionContent class="bg-slate-800 rounded-md p-4">
          <div v-for="(winner, index) in winners3" :key="index" class="border-b border-muted mb-2 pb-2">
            <p class="font-bold">Nome: {{ winner.name }}</p>
            <p class="text-muted">CPF: {{ winner.cpf }}</p>
            <p class="text-muted">Número da sorte: {{ winner.luckyNumber }}</p>
            <p class="text-muted">Prêmio: {{ winner.prize }}</p>
          </div>
        </AccordionContent>
      </AccordionItem>
    </Accordion>
  </div>
</template>

<script setup lang="ts">
import { ref, onMounted } from 'vue';
import { Accordion, AccordionItem, AccordionTrigger, AccordionContent } from '@/components/ui/accordion';
import axios from 'axios';

const winners1 = ref([]);
const winners2 = ref([]);
const winners3 = ref([]);

const fetchWinners = async () => {
  try {
    const response1 = await axios.get('https://api.exemplo.com/winners/sorteio-1');
    const response2 = await axios.get('https://api.exemplo.com/winners/sorteio-2');
    const response3 = await axios.get('https://api.exemplo.com/winners/sorteio-3');

    winners1.value = response1.data;
    winners2.value = response2.data;
    winners3.value = response3.data;
  } catch (error) {
    console.error('Error fetching winners:', error);
  }
};

onMounted(fetchWinners);
</script>

<style scoped></style>