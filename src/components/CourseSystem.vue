<template>
  <section id="courses" class="py-20 md:py-28 bg-surface">
    <div class="section-container">
      <h2 class="section-title scroll-animate">
        课程<span class="gradient-text">体系</span>
      </h2>
      <p class="section-subtitle scroll-animate">
        基于国际顶尖高校AI赋能课程框架，融合本土实践经验，构建"1+3+X"系统化课程体系
      </p>

      <div class="scroll-animate">
        <t-tabs v-model="activeTab" class="custom-tabs">
          <t-tab-panel
            v-for="tab in tabs"
            :key="tab.value"
            :value="tab.value"
            :label="tab.label"
          >
            <div class="bg-white rounded-2xl p-6 md:p-10 mt-2 shadow-sm border border-gray-100">
              <!-- Core Course -->
              <div class="mb-8 p-6 rounded-xl bg-gradient-to-r from-primary to-primary-dark text-white">
                <div class="flex items-center gap-3 mb-3">
                  <Star :size="22" class="text-accent" />
                  <span class="text-sm font-semibold text-white/80 uppercase tracking-wider">核心课程</span>
                </div>
                <h3 class="text-xl md:text-2xl font-bold">{{ tab.core.title }}</h3>
                <p class="mt-2 text-white/80 text-sm leading-relaxed">{{ tab.core.desc }}</p>
              </div>

              <!-- Basic Courses -->
              <div class="mb-8">
                <h4 class="text-lg font-semibold text-gray-900 mb-4 flex items-center gap-2">
                  <Layers :size="18" class="text-primary" />
                  基础课程
                </h4>
                <div class="grid grid-cols-1 md:grid-cols-3 gap-4">
                  <div
                    v-for="course in tab.basic"
                    :key="course.title"
                    class="p-5 rounded-xl bg-surface hover:bg-primary/5 border border-gray-100 hover:border-primary/30 transition-all duration-300 group"
                  >
                    <div class="flex items-center gap-2 mb-2">
                      <div class="w-8 h-8 rounded-lg bg-primary/10 flex items-center justify-center group-hover:bg-primary/20 transition-colors">
                        <BookOpenText :size="16" class="text-primary" />
                      </div>
                      <span class="text-sm font-semibold text-primary">{{ course.tag }}</span>
                    </div>
                    <h5 class="font-semibold text-gray-900 mb-1">{{ course.title }}</h5>
                    <p class="text-sm text-gray-500 leading-relaxed">{{ course.desc }}</p>
                  </div>
                </div>
              </div>

              <!-- Practice Courses -->
              <div>
                <h4 class="text-lg font-semibold text-gray-900 mb-4 flex items-center gap-2">
                  <Zap :size="18" class="text-accent" />
                  实践课程
                </h4>
                <div class="flex flex-wrap gap-3">
                  <span
                    v-for="course in tab.practice"
                    :key="course"
                    class="inline-flex items-center gap-1.5 px-4 py-2 rounded-full bg-surface border border-gray-200 text-sm text-gray-700 hover:border-accent hover:text-accent-dark transition-colors cursor-default"
                  >
                    <CheckCircle :size="14" />
                    {{ course }}
                  </span>
                </div>
              </div>
            </div>
          </t-tab-panel>
        </t-tabs>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import { ref } from 'vue'
import { Star, Layers, BookOpenText, Zap, CheckCircle } from 'lucide-vue-next'

const activeTab = ref('enterprise')

const tabs = [
  {
    value: 'enterprise',
    label: '企业课程',
    target: '企业高层管理者、决策者、技术领导者及中高层管理人员',
    core: {
      title: 'AI领导力与企业战略布局',
      desc: '帮助企业管理者系统构建AI战略思维，制定AI转型路线图，推动组织层面的AI赋能与变革。',
    },
    basic: [
      {
        tag: '基础I',
        title: 'AI基础知识与行业发展',
        desc: '全面了解AI技术发展脉络、核心概念及行业应用趋势',
      },
      {
        tag: '基础II',
        title: 'AI管理与创新思维',
        desc: '掌握AI时代管理思维变革方法，激发组织创新活力',
      },
      {
        tag: '基础III',
        title: 'AI团队建设与人才管理',
        desc: '构建AI时代高效团队模型，优化人才梯队与管理机制',
      },
    ],
    practice: [
      'AI项目实战与案例分析',
      'AI伦理与法规政策',
      'AI跨行业融合与应用',
      '企业AI转型路径规划',
      'AI领导力哲学思想游学',
    ],
  },
  {
    value: 'university',
    label: '高校 & 商学院',
    target: '商学院本科生、研究生、MBA学员、教师和研究人员',
    core: {
      title: 'AI领导力与商业创新',
      desc: '为未来商业领袖提供AI时代的战略视野与创新方法论，培养具备AI素养的复合型人才。',
    },
    basic: [
      {
        tag: '基础I',
        title: 'AI技术概述与商业应用',
        desc: '系统学习AI核心技术原理及其在商业场景中的落地应用',
      },
      {
        tag: '基础II',
        title: 'AI战略管理',
        desc: '掌握AI战略制定与执行方法论，构建系统化的战略框架',
      },
      {
        tag: '基础III',
        title: 'AI领导力与组织变革',
        desc: '深入理解AI驱动下的组织变革路径与领导力新范式',
      },
    ],
    practice: [
      'AI商业案例分析',
      'AI创业指导',
      'AI领导力实训营',
      '跨界合作与资源整合',
      'AI时代商业伦理与责任',
    ],
  },
  {
    value: 'youth',
    label: '青少年课程',
    target: '中小学生、高中生及对科技领域感兴趣的青少年',
    core: {
      title: 'AI启蒙与领导力培养',
      desc: '激发青少年对AI技术的兴趣，培养计算思维与领导力素养，为未来AI时代做好准备。',
    },
    basic: [
      {
        tag: '基础I',
        title: 'AI基础知识普及',
        desc: '以生动有趣的方式了解AI的基本概念、发展历史和日常应用',
      },
      {
        tag: '基础II',
        title: 'AI思维与创新方法',
        desc: '培养逻辑思维和创造性解决问题的能力，掌握基础创新方法论',
      },
      {
        tag: '基础III',
        title: '团队协作与领导力训练',
        desc: '通过项目实践提升团队协作能力，锻炼表达、沟通和领导力',
      },
    ],
    practice: [
      'AI编程实践',
      'AI项目设计与制作',
      'AI科普讲座与研讨会',
      'AI竞赛与创新创业活动',
      'AI职业规划与成长指导',
    ],
  },
]
</script>

<style scoped>
.custom-tabs :deep(.t-tabs__header) {
  background: transparent;
}

.custom-tabs :deep(.t-tabs__nav-wrap) {
  justify-content: center;
}

.custom-tabs :deep(.t-tabs__item) {
  font-size: 1rem;
  font-weight: 600;
  padding: 12px 28px;
  color: var(--text-secondary);
  transition: all 0.3s ease;
}

.custom-tabs :deep(.t-tabs__item--active) {
  color: var(--primary) !important;
}

.custom-tabs :deep(.t-tabs__active-bar) {
  background-color: var(--primary);
}
</style>
