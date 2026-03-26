<template>
  <footer class="bg-dark-deep text-white/70 py-12">
    <div class="section-container">
      <div class="grid grid-cols-1 md:grid-cols-3 gap-8 mb-8">
        <!-- Brand -->
        <div>
          <div class="flex items-center gap-2 mb-4">
            <div class="w-9 h-9 rounded-lg bg-primary flex items-center justify-center font-bold text-white">智</div>
            <span class="text-lg font-bold text-white">智午研究院</span>
          </div>
          <p class="text-sm leading-relaxed text-white/50">
            智午研究院（since 2010）致力于数字经济、AI领导力及数字化转型领域的研究与教育，为企业与个人提供前沿的AI赋能方案。
          </p>
        </div>

        <!-- Quick Links -->
        <div>
          <h4 class="text-white font-semibold mb-4">快速导航</h4>
          <ul class="space-y-2 text-sm">
            <li><a href="#instructor" class="hover:text-white transition-colors">讲师介绍</a></li>
            <li><a href="#courses" class="hover:text-white transition-colors">课程体系</a></li>
            <li><a href="#cases" class="hover:text-white transition-colors">案例展示</a></li>
            <li><a href="#videos" class="hover:text-white transition-colors">课程视频</a></li>
          </ul>
        </div>

        <!-- Social / Contact -->
        <div>
          <h4 class="text-white font-semibold mb-4">关注我们</h4>
          <p class="text-sm text-white/50 mb-3">获取最新课程资讯与行业洞察</p>
          <div class="flex gap-3">
            <a href="#" class="w-9 h-9 rounded-lg bg-white/5 hover:bg-primary/30 border border-white/10 flex items-center justify-center transition-colors">
              <MessageCircle :size="16" class="text-white/60" />
            </a>
            <a href="#" class="w-9 h-9 rounded-lg bg-white/5 hover:bg-primary/30 border border-white/10 flex items-center justify-center transition-colors">
              <Globe :size="16" class="text-white/60" />
            </a>
            <a href="#" class="w-9 h-9 rounded-lg bg-white/5 hover:bg-primary/30 border border-white/10 flex items-center justify-center transition-colors">
              <Mail :size="16" class="text-white/60" />
            </a>
          </div>
        </div>
      </div>

      <!-- Divider & Copyright -->
      <div class="border-t border-white/10 pt-8 flex flex-col md:flex-row items-center justify-between gap-4">
        <p class="text-sm text-white/40">
          &copy; {{ new Date().getFullYear() }} 智午研究院 All Rights Reserved.
        </p>
        <div class="flex items-center gap-6 text-sm text-white/40">
          <a href="#" class="hover:text-white/70 transition-colors">隐私政策</a>
          <a href="#" class="hover:text-white/70 transition-colors">使用条款</a>
          <a href="#" class="hover:text-white/70 transition-colors">京ICP备XXXXXXXX号</a>
        </div>
      </div>
    </div>
  </footer>
</template>

<script setup lang="ts">
import { MessageCircle, Globe, Mail } from 'lucide-vue-next'
</script>
