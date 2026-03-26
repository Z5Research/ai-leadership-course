<template>
  <section id="cases" class="py-20 md:py-28 bg-white">
    <div class="section-container">
      <h2 class="section-title scroll-animate">
        案例<span class="gradient-text">展示</span>
      </h2>
      <p class="section-subtitle scroll-animate">
        服务众多政府机构及世界500强企业，提供AI转型战略规划与高管赋能培训
      </p>

      <!-- Client Logo Wall -->
      <div class="scroll-animate mb-16">
        <div class="grid grid-cols-2 sm:grid-cols-4 lg:grid-cols-8 gap-4">
          <div
            v-for="(client, index) in clients"
            :key="client.name"
            class="group flex flex-col items-center justify-center p-4 rounded-xl bg-surface border border-gray-100 hover:border-primary/20 hover:bg-white hover:shadow-md transition-all duration-300"
            :style="{ transitionDelay: index * 0.05 + 's' }"
          >
            <component :is="client.icon" :size="28" class="text-gray-400 group-hover:text-primary transition-colors mb-2" />
            <span class="text-xs font-medium text-gray-500 group-hover:text-gray-900 transition-colors text-center leading-tight">
              {{ client.name }}
            </span>
          </div>
        </div>
      </div>

      <!-- Case Cards -->
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
        <div
          v-for="(caseItem, index) in caseItems"
          :key="caseItem.title"
          class="scroll-animate group"
          :style="{ transitionDelay: index * 0.1 + 's' }"
        >
          <div class="p-6 rounded-2xl bg-white border border-gray-100 hover:border-primary/20 shadow-sm hover:shadow-lg transition-all duration-300 h-full flex flex-col">
            <div class="flex items-center gap-3 mb-4">
              <div
                class="px-3 py-1 rounded-full text-xs font-semibold"
                :class="caseItem.tagClass"
              >
                {{ caseItem.tag }}
              </div>
              <span class="text-xs text-gray-400">{{ caseItem.type }}</span>
            </div>

            <div class="w-10 h-10 rounded-lg bg-primary/10 flex items-center justify-center mb-4">
              <component :is="caseItem.icon" :size="20" class="text-primary" />
            </div>

            <h3 class="text-lg font-bold text-gray-900 mb-2">{{ caseItem.title }}</h3>
            <p class="text-sm text-gray-500 leading-relaxed flex-1">{{ caseItem.desc }}</p>

            <div class="mt-4 pt-4 border-t border-gray-50 flex flex-wrap gap-2">
              <span
                v-for="kw in caseItem.keywords"
                :key="kw"
                class="px-2.5 py-1 rounded bg-surface text-xs text-gray-500"
              >
                {{ kw }}
              </span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import { Building, Shield, Radio, Smartphone, Globe, Server, Car, Search } from 'lucide-vue-next'

const clients = [
  { name: '中国建材', icon: Building },
  { name: '中国再保险', icon: Shield },
  { name: '中国移动', icon: Radio },
  { name: '中国联通', icon: Smartphone },
  { name: '中国电信', icon: Radio },
  { name: '新浪', icon: Globe },
  { name: '360集团', icon: Server },
  { name: '比亚迪', icon: Car },
]

const caseItems = [
  {
    tag: '能源行业',
    tagClass: 'bg-blue-50 text-blue-600',
    type: 'AI战略规划',
    icon: Zap,
    title: '大型能源集团AI转型战略规划',
    desc: '为某大型能源集团制定全面的AI转型战略，涵盖智能运维、智能调度、智能客服等核心业务场景，帮助其实现数字化转型目标。',
    keywords: ['AI战略', '智能运维', '流程优化'],
  },
  {
    tag: '金融行业',
    tagClass: 'bg-green-50 text-green-600',
    type: '高管AI赋能培训',
    icon: TrendingUp,
    title: '保险行业高管AI领导力培训',
    desc: '为某大型保险集团中高层管理者提供系统化AI领导力培训，涵盖AI技术应用、数据驱动决策、风控智能化等核心模块。',
    keywords: ['领导力提升', '数据驱动', '风控智能'],
  },
  {
    tag: '科技行业',
    tagClass: 'bg-purple-50 text-purple-600',
    type: 'AI产品创新咨询',
    icon: Lightbulb,
    title: '互联网企业AI产品创新咨询',
    desc: '协助某头部互联网企业进行AI产品战略规划与创新咨询，推动AI技术在核心业务线中的深度集成与应用。',
    keywords: ['产品创新', 'AI集成', '业务赋能'],
  },
]

// Re-import icons used in case items
import { Zap, TrendingUp, Lightbulb } from 'lucide-vue-next'
</script>
