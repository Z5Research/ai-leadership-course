<template>
  <section id="cta" class="py-20 md:py-28 relative overflow-hidden">
    <!-- Background -->
    <div class="absolute inset-0 bg-gradient-to-br from-primary-dark via-primary to-dark-purple"></div>
    <div class="absolute inset-0 overflow-hidden opacity-10">
      <div class="grid-pattern absolute inset-0"></div>
    </div>
    <div class="absolute top-10 right-10 w-72 h-72 bg-accent/10 rounded-full blur-3xl"></div>
    <div class="absolute bottom-10 left-10 w-96 h-96 bg-primary/20 rounded-full blur-3xl"></div>

    <div class="relative z-10 section-container text-center">
      <div class="scroll-animate">
        <div class="inline-block px-4 py-1.5 rounded-full bg-white/10 backdrop-blur-sm border border-white/20 text-white/90 text-sm font-medium mb-8">
          开启AI领导力之旅
        </div>

        <h2 class="text-3xl md:text-5xl font-bold text-white mb-6 text-shadow-lg leading-tight">
          让AI成为企业<br class="hidden sm:block" />
          <span class="text-accent">核心竞争力</span>
        </h2>

        <p class="text-lg text-white/70 max-w-2xl mx-auto mb-10 leading-relaxed">
          无论您是寻求AI转型的企业决策者，还是希望提升AI素养的管理人才，我们都能为您提供量身定制的解决方案
        </p>

        <!-- Contact Cards -->
        <div class="grid grid-cols-1 sm:grid-cols-3 gap-4 max-w-3xl mx-auto mb-12">
          <div class="p-5 rounded-xl bg-white/10 backdrop-blur-sm border border-white/10 hover:bg-white/15 transition-colors">
            <Phone :size="24" class="text-accent mx-auto mb-3" />
            <p class="text-sm text-white/50 mb-1">电话咨询</p>
            <p class="text-white font-semibold">400-888-0000</p>
          </div>
          <div class="p-5 rounded-xl bg-white/10 backdrop-blur-sm border border-white/10 hover:bg-white/15 transition-colors">
            <Mail :size="24" class="text-accent mx-auto mb-3" />
            <p class="text-sm text-white/50 mb-1">邮箱联系</p>
            <p class="text-white font-semibold">contact@zhiwu.ai</p>
          </div>
          <div class="p-5 rounded-xl bg-white/10 backdrop-blur-sm border border-white/10 hover:bg-white/15 transition-colors">
            <MessageCircle :size="24" class="text-accent mx-auto mb-3" />
            <p class="text-sm text-white/50 mb-1">微信咨询</p>
            <p class="text-white font-semibold">zhiwu_research</p>
          </div>
        </div>

        <!-- CTA Buttons -->
        <div class="flex flex-col sm:flex-row items-center justify-center gap-4">
          <button class="group px-10 py-4 bg-accent hover:bg-accent-dark text-white font-bold rounded-full transition-all hover:shadow-xl hover:shadow-accent/30 hover:scale-105 flex items-center gap-2 text-lg">
            <span>立即预约</span>
            <ArrowRight :size="20" class="transition-transform group-hover:translate-x-1" />
          </button>
          <button class="px-10 py-4 bg-white/10 hover:bg-white/20 backdrop-blur-sm border border-white/30 text-white font-semibold rounded-full transition-all hover:scale-105">
            下载课程手册
          </button>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import { Phone, Mail, MessageCircle, ArrowRight } from 'lucide-vue-next'
</script>

<style scoped>
.grid-pattern {
  background-image:
    linear-gradient(rgba(255, 255, 255, 0.05) 1px, transparent 1px),
    linear-gradient(90deg, rgba(255, 255, 255, 0.05) 1px, transparent 1px);
  background-size: 40px 40px;
}
</style>
