<template>
    <div id="home" class="relative flex items-center justify-center min-h-screen bg-cover bg-center bg-fixed"
        style="background-image: url('https://www.bitmag.com.br/wp-content/uploads/2022/12/andre-tan-fGEEJ7Z8cIA-unsplash-scaled.jpg');">
        <div class="absolute inset-0 bg-black opacity-70"></div>
        <div class="relative z-10 text-center text-white p-6 md:p-16 lg:p-20">
            <h1 class="text-5xl xl:text-7xl font-bold">Participe do Nosso Sorteio!</h1>
            <p class="mt-6 md:text-base xl:text-2xl leading-relaxed max-w-3xl mx-auto">
                Concorra a computadores e componentes eletrônicos incríveis. Junte-se a nós e transforme sua experiência digital com novas tecnologias!
            </p>
            <RegisterButton />
        </div>
    </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
    name: "HeroSection",
});
</script>

<style scoped>
</style>