<template>
  <section id="videos" class="py-20 md:py-28 bg-dark">
    <div class="section-container">
      <h2 class="section-title scroll-animate text-white">
        课程<span class="gold-gradient-text">精选</span>
      </h2>
      <p class="section-subtitle scroll-animate !text-white/60">
        精选课程实录与专题分享，感受刘言午老师独特的授课魅力与深邃洞察
      </p>

      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
        <div
          v-for="(video, index) in videos"
          :key="video.title"
          class="scroll-animate group cursor-pointer"
          :style="{ transitionDelay: index * 0.1 + 's' }"
        >
          <div class="rounded-2xl overflow-hidden bg-dark-purple border border-white/5 hover:border-white/20 transition-all duration-500 hover:shadow-2xl hover:shadow-primary/10">
            <!-- Video Thumbnail -->
            <div class="relative aspect-video overflow-hidden">
              <img
                :src="video.thumbnail"
                :alt="video.title"
                class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-110"
                loading="lazy"
              />
              <div class="absolute inset-0 bg-gradient-to-t from-dark-purple/80 via-transparent to-transparent"></div>

              <!-- Play Button -->
              <div class="absolute inset-0 flex items-center justify-center">
                <div class="w-16 h-16 rounded-full bg-white/20 backdrop-blur-md border border-white/30 flex items-center justify-center transition-all duration-300 group-hover:scale-110 group-hover:bg-accent/90 group-hover:border-accent">
                  <Play :size="24" class="text-white ml-1" />
                </div>
              </div>

              <!-- Duration -->
              <span class="absolute bottom-3 right-3 px-2 py-0.5 rounded bg-black/60 text-white text-xs font-medium">
                {{ video.duration }}
              </span>
            </div>

            <!-- Video Info -->
            <div class="p-5">
              <div class="flex items-center gap-2 mb-3">
                <span class="px-2.5 py-0.5 rounded-full bg-primary/20 text-primary-light text-xs font-medium">
                  {{ video.tag }}
                </span>
              </div>
              <h3 class="text-white font-bold mb-2 group-hover:text-accent transition-colors line-clamp-2">
                {{ video.title }}
              </h3>
              <p class="text-sm text-white/50 leading-relaxed line-clamp-2">
                {{ video.desc }}
              </p>
            </div>
          </div>
        </div>
      </div>

      <!-- More Videos Link -->
      <div class="scroll-animate mt-12 text-center">
        <button class="inline-flex items-center gap-2 px-8 py-3 rounded-full border border-white/20 text-white/70 hover:text-white hover:border-accent hover:bg-accent/10 transition-all duration-300 font-medium">
          <span>查看更多课程</span>
          <ExternalLink :size="16" />
        </button>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import { Play, ExternalLink } from 'lucide-vue-next'

const videos = [
  {
    title: 'AI领导力：数字时代领导者的关键能力',
    desc: '刘言午老师在图书订货会分享AI领导力的核心框架与实践路径，解读企业在AI时代的领导力变革方向。',
    tag: '主题演讲',
    duration: '45:20',
    thumbnail: 'https://images.unsplash.com/photo-1531482615713-2afd69097998?w=640&h=360&fit=crop',
  },
  {
    title: '从数字经济到AI经济：一场生产力的革命',
    desc: '深度剖析数字经济向AI经济演进的关键路径，解读AI如何重塑产业格局与商业模式。',
    tag: '专题讲座',
    duration: '38:15',
    thumbnail: 'https://images.unsplash.com/photo-1485827404703-89b55fcc595e?w=640&h=360&fit=crop',
  },
  {
    title: 'AI战略思维与企业转型路线图',
    desc: '结合实际案例，讲解企业如何制定AI战略规划，从评估到落地的完整转型方法论。',
    tag: '课程实录',
    duration: '52:30',
    thumbnail: 'https://images.unsplash.com/photo-1553877522-43269d4ea984?w=640&h=360&fit=crop',
  },
]
</script>

<style scoped>
.line-clamp-2 {
  display: -webkit-box;
  -webkit-line-clamp: 2;
  -webkit-box-orient: vertical;
  overflow: hidden;
}
</style>
