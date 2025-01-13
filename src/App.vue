<template>
  <div id="app">
    <HeaderSection />
    <HeroSection />
    <AboutSection />
    <ServicesSection />
    <TestimonialSection />
    <ContactSection />
  </div>
</template>

<script>
import HeaderSection from "./components/HeaderSection.vue";
import HeroSection from "./components/HeroSection.vue";
import AboutSection from "./components/AboutSection.vue";
import ServicesSection from "./components/ServicesSection.vue";
import TestimonialSection from "./components/TestimonialSection.vue";
import ContactSection from "./components/ContactSection.vue";

export default {
  components: {
    HeaderSection,
    HeroSection,
    AboutSection,
    ServicesSection,
    TestimonialSection,
    ContactSection,
  },
};
</script>

<style>
body {
  margin: 0;
  font-family: Arial, sans-serif;
}
</style>
