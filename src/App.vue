<script setup lang="ts">
import { useScrollAnimation } from './composables/useScrollAnimation'
import AppHeader from './components/AppHeader.vue'
import HeroBanner from './components/HeroBanner.vue'
import BrandAdvantages from './components/BrandAdvantages.vue'
import CourseSystem from './components/CourseSystem.vue'
import InstructorIntro from './components/InstructorIntro.vue'
import InstructorStyle from './components/InstructorStyle.vue'
import CaseShowcase from './components/CaseShowcase.vue'
import CourseVideo from './components/CourseVideo.vue'
import CtaSection from './components/CtaSection.vue'
import AppFooter from './components/AppFooter.vue'

useScrollAnimation()
</script>

<template>
  <div id="lyw-landing">
    <AppHeader />
    <main>
      <HeroBanner />
      <BrandAdvantages />
      <CourseSystem />
      <InstructorIntro />
      <InstructorStyle />
      <CaseShowcase />
      <CourseVideo />
      <CtaSection />
    </main>
    <AppFooter />
  </div>
</template>
