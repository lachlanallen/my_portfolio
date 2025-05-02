<script setup>
//Import Components Asynchronously
import {  defineAsyncComponent } from 'vue';
const HeroSection = defineAsyncComponent(() => import('@/components/HeroSection.vue'));
const AboutSection = defineAsyncComponent(() => import('@/components/AboutSection.vue'));
const ExperienceSection = defineAsyncComponent(() => import('@/components/ExperienceSection.vue'));
const ProjectSection = defineAsyncComponent(() => import('@/components/ProjectSection.vue'));
const FooterSection = defineAsyncComponent(() => import('@/components/FooterSection.vue'));

</script>

<template>
  <HeroSection />
  <AboutSection />
  <ExperienceSection />
  <ProjectSection />
  <FooterSection id="contact"/> 
</template>
