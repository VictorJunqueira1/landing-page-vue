<script setup lang="ts">
import { Card, CardContent } from '@/components/ui/card';
import { Carousel, CarouselContent, CarouselItem, CarouselNext, CarouselPrevious } from '@/components/ui/carousel';
import RegisterButton from '@/components/RegisterButton.vue';

const prizes = [
  'https://www.pichauarena.com.br/wp-content/uploads/2022/03/Pczinho.png',
  'https://www.pichauarena.com.br/wp-content/uploads/2020/01/8-PC-Gamer-2600-Reais.00_07_35_24.Quadro012.jpg',
  'https://i.pinimg.com/originals/a2/94/b5/a294b593769b6bf61b55c152032e7459.jpg',
  'https://t2.tudocdn.net/661274?w=1920',
  'https://img.odcdn.com.br/wp-content/uploads/2023/11/od-ofertas-controles.jpg',
];

const prizeDescriptions = [
  'Computador Gamer 1',
  'Computador Gamer 2',
  'Kit Periféricos',
  'Controle XBOX 360',
  'Controle PS5 ou XBOX One',
];
</script>

<template>
  <div class="py-16 h-full w-full bg-slate-900" id="prizes">
    <div class="text-center mb-10 space-y-4">
      <h2 class="text-5xl font-bold text-white">Prêmios Incríveis</h2>
      <p class="text-lg text-gray-300">Veja os prêmios que você pode ganhar!</p>
    </div>
    <Carousel class="relative w-full max-w-7xl mx-auto" :opts="{
      align: 'start',
      loop: true,
    }">
      <CarouselContent class="flex gap-4">
        <CarouselItem v-for="(prize, index) in prizes" :key="index"
          class="md:basis-1/2 xl:basis-1/3 2xl:basis-1/4 transition-transform duration-300 ease-in-out">
          <div class="p-3">
            <Card class="bg-white shadow-lg rounded-lg overflow-hidden hover:shadow-2xl transition-all duration-300">
              <CardContent class="p-0">
                <img :src="prize" alt="Prêmio"
                  class="object-cover w-full h-60 transition-transform duration-300 hover:scale-110" />
              </CardContent>
              <div class="p-4 text-center">
                <p class="text-lg font-semibold text-gray-700">{{ prizeDescriptions[index] }}</p>
              </div>
            </Card>
          </div>
        </CarouselItem>
      </CarouselContent>

      <CarouselPrevious
        class="absolute left-0 top-1/2 transform -translate-y-1/2 p-2 bg-indigo-800 text-white rounded-full hover:bg-indigo-700 transition-colors shadow-md hover:shadow-lg" />
      <CarouselNext
        class="absolute right-0 top-1/2 transform -translate-y-1/2 p-2 bg-indigo-800 text-white rounded-full hover:bg-indigo-700 transition-colors shadow-md hover:shadow-lg" />
    </Carousel>

    <div class="text-center text-white py-6 rounded-lg mx-auto max-w-4xl mb-10">
      <h3 class="text-2xl font-semibold mb-2">São 2 computadores GAMERS incríveis!</h3>
      <p class="text-lg max-w-xl mx-auto">Além disso, você pode ganhar mouses gamers, controles de console como XBOX e
        PS5, e muito mais!
        Não perca essa oportunidade de transformar sua experiência de jogo.</p>
    </div>

    <div class="text-center mt-12">
      <RegisterButton />
    </div>
  </div>
</template>