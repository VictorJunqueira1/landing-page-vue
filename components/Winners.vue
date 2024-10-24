<template>
  <div class="p-6 border-t border-gray-800 shadow-md text-white mx-auto max-w-7xl mb-32" id="winners">
    <h1
      class="text-4xl font-bold mt-24 mb-12 text-center bg-gradient-to-r from-blue-500 to-indigo-700 bg-clip-text text-transparent">
      GANHADORES
    </h1>
    <Accordion type="single" collapsible class="w-full">
      <AccordionItem class="mb-4" value="sorteio-1">
        <AccordionTrigger
          class="flex justify-between items-center font-semibold border border-gray-800 mb-2 rounded-lg bg-slate-900 text-xl cursor-pointer">
          <span class="px-4">1º SORTEIO 05/01/2024</span>
        </AccordionTrigger>
        <AccordionContent class="bg-slate-800 rounded-md p-4">
          <div>
            <div v-for="(winner, index) in winners1.slice(0, 3)" :key="index" class="border-b border-muted text-base mb-2 pb-2">
              <p class="font-semibold">Nome: {{ winner.name }}</p>
              <p class="text-gray-400">Prêmio: {{ winner.prize }}</p>
              <p class="text-gray-400">Número da Sorte: 999-999</p>
              <p class="text-gray-400">CPF: ###.###.###-##</p>
            </div>
          </div>
        </AccordionContent>
      </AccordionItem>

      <AccordionItem class="mb-4" value="sorteio-2">
        <AccordionTrigger
          class="flex justify-between items-center font-semibold border border-gray-800 mb-2 rounded-lg bg-slate-900 text-xl cursor-pointer">
          <span class="px-4">2º SORTEIO 15/02/2024</span>
        </AccordionTrigger>
        <AccordionContent class="bg-slate-800 rounded-md p-4">
          <div>
            <div v-for="(winner, index) in winners2.slice(0, 3)" :key="index" class="border-b border-muted text-base mb-2 pb-2">
              <p class="font-semibold">Nome: {{ winner.name }}</p>
              <p class="text-gray-400">Prêmio: {{ winner.prize }}</p>
              <p class="text-gray-400">Número da Sorte: 999-999</p>
              <p class="text-gray-400">CPF: ###.###.###-##</p>
            </div>
          </div>
        </AccordionContent>
      </AccordionItem>

      <AccordionItem class="mb-4" value="sorteio-3">
        <AccordionTrigger
          class="flex justify-between items-center font-semibold border border-gray-800 mb-2 rounded-lg bg-slate-900 text-xl cursor-pointer">
          <span class="px-4">3º SORTEIO 25/03/2024</span>
        </AccordionTrigger>
        <AccordionContent class="bg-slate-800 rounded-md p-4">
          <div>
            <div v-for="(winner, index) in winners3.slice(0, 3)" :key="index" class="border-b border-muted text-base mb-2 pb-2">
              <p class="font-semibold">Nome: {{ winner.name }}</p>
              <p class="text-gray-400">Prêmio: {{ winner.prize }}</p>
              <p class="text-gray-400">Número da Sorte: 999-999</p>
              <p class="text-gray-400">CPF: ###.###.###-##</p>
            </div>
          </div>
        </AccordionContent>
      </AccordionItem>
    </Accordion>
  </div>
</template>

<script setup lang="ts">
import { ref, onMounted } from 'vue';
import axios from 'axios';
import { Accordion, AccordionItem, AccordionTrigger, AccordionContent } from '@/components/ui/accordion';

const winners1 = ref([]);
const winners2 = ref([]);
const winners3 = ref([]);

const fetchWinners = async () => {
  try {
    const [response1, response2, response3] = await Promise.all([
      axios.get('http://localhost:4000/api/winners/'),
      axios.get('http://localhost:4000/api/winners/'),
      axios.get('http://localhost:4000/api/winners/'),
    ]);

    winners1.value = response1.data;
    winners2.value = response2.data;
    winners3.value = response3.data;
  } catch (error) {
    console.error('Error fetching winners:', error);
  }
};

onMounted(fetchWinners);
</script>

<style scoped>
</style>