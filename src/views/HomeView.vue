<script setup>
  import HeroSection from '../components/HeroSection.vue';
  import InfoSection from '../components/InfoSection.vue';
  import ServiceSection from '../components/ServiceSection.vue';
  import ExperienceSection from '../components/ExperienceSection.vue';
  import AboutUsSection from '../components/AboutUsSection.vue';
</script>

<template>
  <div data-bs-spy="scroll" data-bs-target="#navbar" data-bs-root-margin="0px 0px -40%" data-bs-smooth-scroll="true" tabindex="0">
    <HeroSection />
    <main>
      <InfoSection />
      <ServiceSection />
      <ExperienceSection />
      <AboutUsSection />
    </main>
  </div>
</template>
