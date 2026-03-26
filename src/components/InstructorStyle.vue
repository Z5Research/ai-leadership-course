<template>
  <section class="py-20 md:py-28 bg-surface">
    <div class="section-container">
      <h2 class="section-title scroll-animate">
        授课<span class="gradient-text">风格</span>
      </h2>
      <p class="section-subtitle scroll-animate">
        理论与实践深度融合，国际视野与本土创新并重，打造沉浸式学习体验
      </p>

      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6">
        <div
          v-for="(style, index) in styles"
          :key="style.title"
          class="scroll-animate group"
          :style="{ transitionDelay: index * 0.1 + 's' }"
        >
          <div class="p-6 rounded-2xl bg-white border border-gray-100 h-full hover:shadow-xl hover:-translate-y-2 transition-all duration-500">
            <div
              class="w-12 h-12 rounded-xl flex items-center justify-center mb-5 transition-transform duration-500 group-hover:scale-110"
              :class="style.bgClass"
            >
              <component :is="style.icon" :size="24" :class="style.iconColor" />
            </div>
            <h3 class="text-lg font-bold text-gray-900 mb-3">{{ style.title }}</h3>
            <p class="text-sm text-gray-500 leading-relaxed">{{ style.desc }}</p>
            <div class="mt-4 flex flex-wrap gap-1.5">
              <span
                v-for="kw in style.keywords"
                :key="kw"
                class="px-2.5 py-1 rounded-full text-xs font-medium"
                :class="style.tagClass"
              >
                {{ kw }}
              </span>
            </div>
          </div>
        </div>
      </div>

      <!-- Quote -->
      <div class="scroll-animate mt-16 text-center">
        <div class="inline-block max-w-3xl px-10 py-8 rounded-2xl bg-gradient-to-r from-primary/5 to-accent/5 border border-primary/10">
          <Quote :size="32" class="text-primary/30 mb-3 mx-auto" />
          <p class="text-lg md:text-xl font-medium text-gray-800 leading-relaxed italic">
            "AI不是替代人类的工具，而是放大人类能力的杠杆。领导者需要学会驾驭这股力量，带领组织走向更美好的未来。"
          </p>
          <p class="mt-4 text-sm text-primary font-semibold">—— 刘言午</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import { Lightbulb, Globe, LayoutGrid, MessageCircle, Quote } from 'lucide-vue-next'

const styles = [
  {
    icon: Lightbulb,
    title: '理论实战融合',
    desc: '将近20年一线管理经验融入课程教学，每个理论模型都配有真实企业案例支撑，让学员"学之能用，用之有效"。',
    bgClass: 'bg-primary/10',
    iconColor: 'text-primary',
    tagClass: 'bg-primary/5 text-primary',
    keywords: ['案例驱动', '实战演练', '即学即用'],
  },
  {
    icon: Globe,
    title: '国际视野本土实践',
    desc: '融合耶鲁、斯坦福、MIT等国际顶尖高校AI赋能课程框架，结合中国企业实际场景，打造本土化落地路径。',
    bgClass: 'bg-accent/10',
    iconColor: 'text-accent',
    tagClass: 'bg-accent/5 text-accent-dark',
    keywords: ['全球视角', '本土落地', '跨文化融合'],
  },
  {
    icon: LayoutGrid,
    title: '系统化方法论',
    desc: '独创AI领导力路线图、AI战略框架、AI领导力飞轮等实用工具，帮助学员构建完整的知识体系和行动框架。',
    bgClass: 'bg-green-500/10',
    iconColor: 'text-green-600',
    tagClass: 'bg-green-500/5 text-green-600',
    keywords: ['原创模型', '系统框架', '落地工具'],
  },
  {
    icon: MessageCircle,
    title: '互动启发式教学',
    desc: '采用小组讨论、案例分析、角色扮演等多元化教学方式，充分激发学员参与感和思辨能力，营造高效学习氛围。',
    bgClass: 'bg-purple-500/10',
    iconColor: 'text-purple-600',
    tagClass: 'bg-purple-500/5 text-purple-600',
    keywords: ['小组研讨', '情境模拟', '思维碰撞'],
  },
]
</script>
