<script setup lang="ts">
import MainNav from '@/components/MainNav.vue';
import HeroSection from '@/components/HeroSection.vue';
import HowParticipate from '@/components/HowParticipate.vue';
import Prizes from '@/components/Prizes.vue';
import FAQ from '@/components/FAQ.vue';
import Winners from '@/components/Winners.vue';
import Footer from '@/components/Footer.vue';
</script>

<template>
  <div class="bg-slate-950">
    <header>
      <MainNav />
    </header>
    <main>
      <HeroSection />
      <HowParticipate />
      <Prizes />
      <FAQ />
      <Winners />
      <Footer />
    </main>
  </div>
</template>
