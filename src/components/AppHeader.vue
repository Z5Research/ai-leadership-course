<template>
  <header
    class="fixed top-0 left-0 right-0 z-50 transition-all duration-300"
    :class="scrolled ? 'bg-white/95 backdrop-blur-md shadow-lg' : 'bg-transparent'"
  >
    <div class="section-container flex items-center justify-between h-16 md:h-20">
      <a href="#" class="flex items-center gap-2 group">
        <div
          class="w-9 h-9 rounded-lg flex items-center justify-center font-bold text-white text-lg transition-transform group-hover:scale-110"
          :class="scrolled ? 'bg-primary' : 'bg-white/20 backdrop-blur'"
        >
          智
        </div>
        <span
          class="text-lg font-bold transition-colors"
          :class="scrolled ? 'text-primary' : 'text-white'"
        >
          智午研究院
        </span>
      </a>

      <nav class="hidden md:flex items-center gap-8">
        <a
          v-for="item in navItems"
          :key="item.id"
          :href="'#' + item.id"
          class="text-sm font-medium transition-colors hover:text-primary"
          :class="scrolled ? 'text-gray-700' : 'text-white/90'"
        >
          {{ item.label }}
        </a>
        <a
          href="#cta"
          class="px-5 py-2 rounded-full text-sm font-semibold transition-all hover:shadow-lg hover:scale-105"
          :class="scrolled
            ? 'bg-primary text-white hover:bg-primary-dark'
            : 'bg-accent text-white hover:bg-accent-dark'"
        >
          预约咨询
        </a>
      </nav>

      <button
        class="md:hidden p-2 rounded-lg transition-colors"
        :class="scrolled ? 'text-gray-700 hover:bg-gray-100' : 'text-white hover:bg-white/10'"
        @click="mobileMenuOpen = !mobileMenuOpen"
      >
        <Menu v-if="!mobileMenuOpen" :size="24" />
        <X v-else :size="24" />
      </button>
    </div>

    <!-- Mobile Menu -->
    <transition name="slide-down">
      <div
        v-if="mobileMenuOpen"
        class="md:hidden bg-white/95 backdrop-blur-md border-t border-gray-100 shadow-lg"
      >
        <div class="section-container py-4 flex flex-col gap-3">
          <a
            v-for="item in navItems"
            :key="item.id"
            :href="'#' + item.id"
            class="py-2 px-4 text-gray-700 font-medium rounded-lg hover:bg-primary/5 hover:text-primary transition-colors"
            @click="mobileMenuOpen = false"
          >
            {{ item.label }}
          </a>
          <a
            href="#cta"
            class="py-2 px-4 bg-primary text-white text-center rounded-lg font-semibold"
            @click="mobileMenuOpen = false"
          >
            预约咨询
          </a>
        </div>
      </div>
    </transition>
  </header>
</template>

<script setup lang="ts">
import { ref, onMounted, onUnmounted } from 'vue'
import { Menu, X } from 'lucide-vue-next'

const scrolled = ref(false)
const mobileMenuOpen = ref(false)

const navItems = [
  { id: 'instructor', label: '讲师介绍' },
  { id: 'courses', label: '课程体系' },
  { id: 'cases', label: '案例展示' },
  { id: 'videos', label: '课程视频' },
]

const handleScroll = () => {
  scrolled.value = window.scrollY > 50
}

onMounted(() => {
  window.addEventListener('scroll', handleScroll)
})

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll)
})
</script>

<style scoped>
.slide-down-enter-active,
.slide-down-leave-active {
  transition: all 0.3s ease;
}
.slide-down-enter-from,
.slide-down-leave-to {
  opacity: 0;
  transform: translateY(-10px);
}
</style>
