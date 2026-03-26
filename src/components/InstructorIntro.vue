<template>
  <section id="instructor" class="py-20 md:py-28 bg-white">
    <div class="section-container">
      <h2 class="section-title scroll-animate">
        讲师<span class="gradient-text">介绍</span>
      </h2>
      <p class="section-subtitle scroll-animate">
        国内较早提出"AI领导力"概念的实战型学者，致力于推动人工智能在企业管理与教育中的应用
      </p>

      <div class="scroll-animate grid grid-cols-1 lg:grid-cols-5 gap-10 items-start">
        <!-- Left: Avatar & Info -->
        <div class="lg:col-span-2">
          <div class="sticky top-28">
            <!-- Avatar -->
            <div class="relative w-48 h-48 mx-auto mb-8">
              <div class="absolute inset-0 rounded-full bg-gradient-to-br from-primary via-accent to-primary-dark animate-pulse-glow"></div>
              <div class="relative w-48 h-48 rounded-full bg-gradient-to-br from-primary-dark to-dark-purple flex items-center justify-center border-4 border-white shadow-xl">
                <span class="text-5xl font-bold text-white">刘</span>
              </div>
              <div class="absolute -bottom-2 -right-2 w-14 h-14 bg-accent rounded-full flex items-center justify-center shadow-lg">
                <Award :size="24" class="text-white" />
              </div>
            </div>

            <!-- Name & Title -->
            <h3 class="text-2xl font-bold text-center text-gray-900 mb-2">刘言午</h3>
            <p class="text-center text-primary font-semibold mb-4">AI领导力导师 · 管理学者 · 作家</p>

            <!-- Tags -->
            <div class="flex flex-wrap justify-center gap-2 mb-6">
              <span
                v-for="tag in tags"
                :key="tag"
                class="px-3 py-1 rounded-full bg-surface text-xs font-medium text-gray-600"
              >
                {{ tag }}
              </span>
            </div>

            <!-- Credentials -->
            <div class="flex justify-center gap-4 text-sm text-gray-500">
              <span class="flex items-center gap-1"><Shield :size="14" /> PMP</span>
              <span class="flex items-center gap-1"><Shield :size="14" /> MCSE</span>
            </div>
          </div>
        </div>

        <!-- Right: Bio & Books -->
        <div class="lg:col-span-3 space-y-8">
          <!-- Bio -->
          <div class="p-8 rounded-2xl bg-surface border border-gray-100">
            <h4 class="text-lg font-semibold text-gray-900 mb-4 flex items-center gap-2">
              <User :size="20" class="text-primary" />
              个人简介
            </h4>
            <p class="text-gray-600 leading-relaxed mb-4">
              刘言午，管理学者、作家，智午研究院（since 2010）院长。亚太数字经济学会常务理事长，中国技术经济学会高级委员，中国电子信息行业联合会数字经济专委会AI大模型工作组负责人，中国计算机学会委员，中国产学研合作促进会委员。
            </p>
            <p class="text-gray-600 leading-relaxed mb-4">
              拥有近20年技术管理与领导经验，10年以上创业经验。曾管理累计项目额超过50亿元人民币的AI、数字化及智慧化项目。服务客户遍布全球及多业态，具备丰富的行业实战背景。
            </p>
            <p class="text-gray-600 leading-relaxed">
              国内较早提出"AI领导力"概念并深入研究的实战型学者，研究领域涵盖技术管理、数字经济、数字化转型、AI领导力、人工智能应用及案例产业研究。融合耶鲁大学、斯坦福大学、MIT等国际顶尖高校的AI赋能课程框架，构建了系统化的AI领导力课程体系。
            </p>
          </div>

          <!-- Books -->
          <div>
            <h4 class="text-lg font-semibold text-gray-900 mb-4 flex items-center gap-2">
              <BookMarked :size="20" class="text-accent" />
              代表著作
            </h4>
            <div class="grid grid-cols-1 md:grid-cols-2 gap-5">
              <div
                v-for="book in books"
                :key="book.title"
                class="group p-6 rounded-2xl bg-white border border-gray-100 hover:border-primary/30 shadow-sm hover:shadow-lg transition-all duration-300"
              >
                <div class="flex gap-4">
                  <div class="shrink-0 w-20 h-28 rounded-lg bg-gradient-to-br from-primary-dark to-primary flex items-center justify-center shadow-md">
                    <BookOpen :size="28" class="text-white" />
                  </div>
                  <div class="flex-1 min-w-0">
                    <h5 class="font-bold text-gray-900 mb-1 group-hover:text-primary transition-colors">
                      {{ book.title }}
                    </h5>
                    <p class="text-sm text-gray-500 mb-2">{{ book.publisher }}</p>
                    <p class="text-xs text-gray-400">{{ book.date }}</p>
                  </div>
                </div>
                <p class="mt-4 text-sm text-gray-600 leading-relaxed">{{ book.desc }}</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import { Award, Shield, User, BookMarked, BookOpen } from 'lucide-vue-next'

const tags = [
  '智午研究院院长',
  '亚太数字经济学会常务理事长',
  '中国技术经济学会高级委员',
  '中国计算机学会委员',
  'AI大模型工作组负责人',
]

const books = [
  {
    title: 'AI领导力',
    publisher: '中国科学技术出版社',
    date: '2024年11月',
    desc: '提出AI领导力路线图、AI战略框架、AI领导力飞轮等原创工具，获数十位行业专家联袂推荐。系统阐述了AI时代下的领导力转型路径与实战方法论。',
  },
  {
    title: '决胜数字化转型',
    publisher: '中国科学技术出版社',
    date: '2025年2月',
    desc: '翻译自亚马逊解决方案架构师20年行业经验专著，探讨突破企业数字化瓶颈的全盘实操方法论。刘言午负责前三部分翻译工作。',
  },
]
</script>
