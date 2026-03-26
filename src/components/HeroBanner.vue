<template>
  <section class="relative min-h-screen flex items-center justify-center overflow-hidden">
    <!-- Background -->
    <div class="absolute inset-0 bg-gradient-to-br from-dark-purple via-primary-dark to-dark"></div>

    <!-- Grid Animation -->
    <div class="absolute inset-0 overflow-hidden opacity-10">
      <div class="grid-pattern absolute inset-0"></div>
    </div>

    <!-- Floating Orbs -->
    <div class="absolute top-20 left-10 w-72 h-72 bg-primary/20 rounded-full blur-3xl animate-float"></div>
    <div class="absolute bottom-20 right-10 w-96 h-96 bg-accent/10 rounded-full blur-3xl animate-float" style="animation-delay: -3s;"></div>
    <div class="absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2 w-[600px] h-[600px] bg-primary/5 rounded-full blur-3xl animate-pulse-glow"></div>

    <!-- Content -->
    <div class="relative z-10 section-container text-center pt-20">
      <div class="mb-6">
        <span class="inline-block px-4 py-1.5 rounded-full bg-white/10 backdrop-blur-sm border border-white/20 text-white/90 text-sm font-medium">
          《AI领导力》作者 · 智午研究院院长
        </span>
      </div>

      <h1 class="text-5xl md:text-7xl lg:text-8xl font-bold text-white mb-6 text-shadow-lg leading-tight">
        善用AI
        <span class="gold-gradient-text">人人受益</span>
      </h1>

      <p class="text-lg md:text-xl text-white/80 max-w-3xl mx-auto mb-4 leading-relaxed">
        数字化转型资深专家，近20年技术管理与领导经验
      </p>

      <p class="text-base text-white/60 max-w-2xl mx-auto mb-10 leading-relaxed">
        融合耶鲁大学、斯坦福大学、MIT等顶尖高校AI赋能课程框架，为企业高管与组织提供系统化的AI领导力提升方案
      </p>

      <!-- CTA Buttons -->
      <div class="flex flex-col sm:flex-row items-center justify-center gap-4 mb-16">
        <a
          href="#cta"
          class="group px-8 py-4 bg-accent hover:bg-accent-dark text-white font-semibold rounded-full transition-all hover:shadow-xl hover:shadow-accent/30 hover:scale-105 flex items-center gap-2"
        >
          <span>预约咨询</span>
          <ArrowRight :size="18" class="transition-transform group-hover:translate-x-1" />
        </a>
        <a
          href="#courses"
          class="px-8 py-4 bg-white/10 hover:bg-white/20 backdrop-blur-sm border border-white/30 text-white font-semibold rounded-full transition-all hover:scale-105"
        >
          了解课程
        </a>
      </div>

      <!-- Stats -->
      <div class="grid grid-cols-2 md:grid-cols-4 gap-6 max-w-4xl mx-auto">
        <div v-for="stat in stats" :key="stat.label" class="text-center">
          <div class="text-3xl md:text-4xl font-bold text-white mb-1">{{ stat.value }}</div>
          <div class="text-sm text-white/60">{{ stat.label }}</div>
        </div>
      </div>
    </div>

    <!-- Scroll Indicator -->
    <div class="absolute bottom-8 left-1/2 -translate-x-1/2 flex flex-col items-center gap-2 animate-bounce">
      <span class="text-white/40 text-xs">向下滚动</span>
      <ChevronDown :size="20" class="text-white/40" />
    </div>
  </section>
</template>

<script setup lang="ts">
import { ArrowRight, ChevronDown } from 'lucide-vue-next'

const stats = [
  { value: '20年+', label: '技术管理经验' },
  { value: '50亿+', label: '累计项目额' },
  { value: '100+', label: '服务企业' },
  { value: '8大', label: '课程体系' },
]
</script>

<style scoped>
.grid-pattern {
  background-image:
    linear-gradient(rgba(255, 255, 255, 0.05) 1px, transparent 1px),
    linear-gradient(90deg, rgba(255, 255, 255, 0.05) 1px, transparent 1px);
  background-size: 60px 60px;
  animation: gridMove 20s linear infinite;
}

@keyframes gridMove {
  0% { transform: translate(0, 0); }
  100% { transform: translate(60px, 60px); }
}
</style>
