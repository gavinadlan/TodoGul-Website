<template>
  <div id="app">
    <HeaderSection />
    <HeroSection />
    <AboutSection />
    <FeaturesSection />
    <ReviewSection />
    <!-- Updated to ReviewSection -->
    <ContactSection />
    <FooterSection />
  </div>
</template>

<script>
import HeaderSection from "./components/HeaderSection.vue";
import HeroSection from "./components/HeroSection.vue";
import AboutSection from "./components/AboutSection.vue";
import FeaturesSection from "./components/FeaturesSection.vue";
import ReviewSection from "./components/ReviewSection.vue"; // Correct import
import ContactSection from "./components/ContactSection.vue";
import FooterSection from "./components/FooterSection.vue";

export default {
  components: {
    HeaderSection,
    HeroSection,
    AboutSection,
    FeaturesSection,
    ReviewSection, // Correct component registration
    ContactSection,
    FooterSection,
  },
};
</script>

<style>
body {
  margin: 0;
  font-family: Arial, sans-serif;
}
</style>
