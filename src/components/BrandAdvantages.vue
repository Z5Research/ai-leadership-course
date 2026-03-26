<template>
  <section class="py-20 md:py-28 bg-white">
    <div class="section-container">
      <h2 class="section-title scroll-animate">
        核心<span class="gradient-text">优势</span>
      </h2>
      <p class="section-subtitle scroll-animate">
        深厚的学术积淀与丰富的实战经验，为企业和组织提供值得信赖的AI转型方案
      </p>

      <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-6">
        <div
          v-for="(item, index) in advantages"
          :key="item.title"
          class="scroll-animate group p-8 rounded-2xl border border-gray-100 bg-white hover:bg-primary hover:border-primary transition-all duration-500 hover:shadow-xl hover:shadow-primary/20 hover:-translate-y-2 cursor-default"
          :style="{ transitionDelay: index * 0.1 + 's' }"
        >
          <div
            class="w-14 h-14 rounded-xl flex items-center justify-center mb-5 transition-colors duration-500"
            :class="item.bgClass"
          >
            <component :is="item.icon" :size="28" :class="item.iconClass" />
          </div>
          <div
            class="text-3xl font-bold mb-2 transition-colors duration-500"
            :class="item.valueClass"
          >
            {{ item.value }}
          </div>
          <h3
            class="text-lg font-semibold mb-2 transition-colors duration-500"
            :class="item.titleClass"
          >
            {{ item.title }}
          </h3>
          <p
            class="text-sm leading-relaxed transition-colors duration-500"
            :class="item.descClass"
          >
            {{ item.desc }}
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import { Award, TrendingUp, BookOpen, Building2 } from 'lucide-vue-next'

const advantages = [
  {
    icon: Award,
    value: '20年+',
    title: '技术管理经验',
    desc: '近20年技术管理与领导经验，10年以上创业经历，深耕数字经济与AI领域',
    bgClass: 'bg-primary/10',
    iconClass: 'text-primary group-hover:text-white',
    valueClass: 'text-primary group-hover:text-white',
    titleClass: 'text-gray-900 group-hover:text-white',
    descClass: 'text-gray-500 group-hover:text-white/80',
  },
  {
    icon: TrendingUp,
    value: '50亿+',
    title: '累计项目额',
    desc: '曾管理累计项目额超过50亿元人民币的AI、数字化及智慧化项目',
    bgClass: 'bg-accent/10',
    iconClass: 'text-accent group-hover:text-white',
    valueClass: 'text-accent group-hover:text-white',
    titleClass: 'text-gray-900 group-hover:text-white',
    descClass: 'text-gray-500 group-hover:text-white/80',
  },
  {
    icon: BookOpen,
    value: '8大',
    title: '课程体系',
    desc: '涵盖企业高管、高校商学院、青少年三大人群，提供系统化AI领导力教育',
    bgClass: 'bg-green-500/10',
    iconClass: 'text-green-600 group-hover:text-white',
    valueClass: 'text-green-600 group-hover:text-white',
    titleClass: 'text-gray-900 group-hover:text-white',
    descClass: 'text-gray-500 group-hover:text-white/80',
  },
  {
    icon: Building2,
    value: '100+',
    title: '服务企业',
    desc: '服务中国建材、中国移动、360集团、比亚迪等多家政府及500强企业',
    bgClass: 'bg-purple-500/10',
    iconClass: 'text-purple-600 group-hover:text-white',
    valueClass: 'text-purple-600 group-hover:text-white',
    titleClass: 'text-gray-900 group-hover:text-white',
    descClass: 'text-gray-500 group-hover:text-white/80',
  },
]
</script>
