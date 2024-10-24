<template>
  <div class="p-6 border-t border-gray-800 shadow-md text-white mx-auto max-w-7xl mb-32" id="winners">
    <h1
      class="text-4xl font-bold mt-24 mb-12 text-center bg-gradient-to-r from-blue-500 to-indigo-700 bg-clip-text text-transparent">
      GANHADORES
    </h1>
    <Accordion type="single" collapsible class="w-full">
      <AccordionItem class="mb-4" value="winners">
        <AccordionTrigger
          class="flex justify-between items-center font-semibold border border-gray-800 mb-2 rounded-lg bg-slate-900 text-xl cursor-pointer">
          <span class="px-4">1° SORTEIO 05/01/2024</span>
        </AccordionTrigger>
        <AccordionContent class="bg-slate-800 rounded-md p-4">
          <div>
            <div v-for="(winner, index) in winners" :key="index" class="border-b border-muted text-base mb-2 pb-2">
              <p class="font-semibold">Nome: {{ winner.name }}</p>
              <p class="text-gray-300">Prêmio: {{ winner.prize }}</p>
              <p class="text-gray-300">CPF: ###.###.###-##</p>
              <p class="text-gray-300">Número da Sorte: 999 - 999</p>
            </div>
          </div>
        </AccordionContent>
      </AccordionItem>
    </Accordion>
    <Accordion type="single" collapsible class="w-full">
      <AccordionItem class="mb-4" value="winners">
        <AccordionTrigger
          class="flex justify-between items-center font-semibold border border-gray-800 mb-2 rounded-lg bg-slate-900 text-xl cursor-pointer">
          <span class="px-4">2° SORTEIO 12/01/2024</span>
        </AccordionTrigger>
        <AccordionContent class="bg-slate-800 rounded-md p-4">
          <div>
            <div class="border-b border-muted text-base mb-2 pb-2">
              <p class="font-semibold">SORTEIO AINDA NÃO REALIZADO</p>
            </div>
          </div>
        </AccordionContent>
      </AccordionItem>
    </Accordion>
    <Accordion type="single" collapsible class="w-full">
      <AccordionItem class="mb-4" value="winners">
        <AccordionTrigger
          class="flex justify-between items-center font-semibold border border-gray-800 mb-2 rounded-lg bg-slate-900 text-xl cursor-pointer">
          <span class="px-4">3° SORTEIO 19/01/2024</span>
        </AccordionTrigger>
        <AccordionContent class="bg-slate-800 rounded-md p-4">
          <div>
            <div class="border-b border-muted text-base mb-2 pb-2">
              <p class="font-semibold">SORTEIO AINDA NÃO REALIZADO</p>
            </div>
          </div>
        </AccordionContent>
      </AccordionItem>
    </Accordion>
  </div>
</template>

<script setup lang="ts">
import { Accordion, AccordionItem, AccordionTrigger, AccordionContent } from '@/components/ui/accordion';
import { onMounted, ref } from '@vue/runtime-core';

const winners = ref([]);

const fetchWinners = async () => {
  try {
    const response = await fetch('http://localhost:4000/api/winners/');
    const data = await response.json();
    winners.value = data;
  } catch (error) {
    console.error('Error fetching winners:', error);
  }
};

onMounted(fetchWinners);
</script>

<style scoped></style>