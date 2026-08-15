<script setup>
import SiteArchiveBar from './components/SiteArchiveBar.vue'
import HeroSection from './components/HeroSection.vue'
import WhySection from './components/WhySection.vue'
import WhatSection from './components/WhatSection.vue'
import HowSection from './components/HowSection.vue'
import BeyondSection from './components/BeyondSection.vue'
</script>

<template>
  <div class="site">
    <SiteArchiveBar />
    <main>
      <HeroSection />
      <WhySection />
      <WhatSection />
      <HowSection />
      <BeyondSection />
    </main>
  </div>
</template>
