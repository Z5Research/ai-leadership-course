# AI领导力课程 - 刘言午老师官方介绍网站

> **AI Leadership Course — Official Website of Instructor Liu Yanwu**
>
> "善用AI，人人受益" — Harness AI, Benefit Everyone

[![Vue 3](https://img.shields.io/badge/Vue-3.5-42b883?logo=vue.js)](https://vuejs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.6-3178c6?logo=typescript)](https://www.typescriptlang.org/)
[![TDesign](https://img.shields.io/badge/TDesign-Vue_Next-0052d9)](https://tdesign.tencent.com/vue-next/overview)
[![Vite](https://img.shields.io/badge/Vite-5.4-646cff?logo=vite)](https://vitejs.dev/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

---

## 📖 项目简介 | Project Overview

本项目是 **刘言午老师**（《AI领导力》《决胜数字化转型》作者）的官方讲师介绍落地页。网站展示了刘言午老师在AI领导力、数字化转型领域的课程体系、学术背景、授课风格、企业合作案例及课程视频等核心内容。

This project is the **official landing page for Instructor Liu Yanwu**, author of *"AI Leadership"* and *"Winning Digital Transformation"*. The website showcases his course systems, academic background, teaching style, enterprise collaboration cases, and course videos in the fields of AI leadership and digital transformation.

---

## ✨ 核心特性 | Key Features

- 🎯 **沉浸式首屏** — 深蓝渐变 + 几何网格动效 + 浮动光晕，打造科技感第一印象
- 📚 **1+3+X 课程体系** — 企业/高校/青少年三大课程体系，TDesign Tabs 交互切换
- 👨‍🏫 **讲师全景展示** — 头衔矩阵、社会职务、著作展示、授课风格全面呈现
- 🏢 **企业案例墙** — 服务500强企业LOGO展示 + 典型案例卡片
- 🎬 **课程视频区** — 视频卡片布局，支持扩展真实视频链接
- 📱 **响应式设计** — 完美适配 PC 与移动端
- 🌊 **滚动动画** — 各区块滚动淡入动效，提升浏览体验
- 🧩 **毛玻璃导航** — 固定顶部导航栏，滚动时背景模糊变化

---

## 🛠 技术栈 | Tech Stack

| 技术 | 版本 | 用途 |
|------|------|------|
| [Vue 3](https://vuejs.org/) | 3.5+ | 前端框架（Composition API） |
| [TypeScript](https://www.typescriptlang.org/) | 5.6+ | 类型安全 |
| [Vite](https://vitejs.dev/) | 5.4+ | 构建工具 |
| [TDesign Vue Next](https://tdesign.tencent.com/vue-next/overview) | 1.18+ | UI 组件库 |
| [Tailwind CSS](https://tailwindcss.com/) | 3.4+ | 原子化 CSS |
| [Lucide Icons](https://lucide.dev/) | 1.0+ | 图标库 |

---

## 📁 项目结构 | Project Structure

```
src/
├── assets/
│   └── styles/
│       └── global.css          # 全局样式、CSS 变量、动画关键帧
├── components/
│   ├── AppHeader.vue           # 固定导航栏（毛玻璃效果）
│   ├── HeroBanner.vue          # 首屏 Banner（渐变 + 动效）
│   ├── BrandAdvantages.vue     # 核心优势区（四大数据卡片）
│   ├── CourseSystem.vue        # 课程体系（TDesign Tabs 切换）
│   ├── InstructorIntro.vue     # 讲师介绍（头衔、职务、著作）
│   ├── InstructorStyle.vue     # 授课风格（四大特点）
│   ├── CaseShowcase.vue        # 案例展示（LOGO 墙 + 案例卡片）
│   ├── CourseVideo.vue         # 课程视频区
│   ├── CtaSection.vue          # 合作咨询 CTA
│   └── AppFooter.vue           # 页脚
├── composables/
│   └── useScrollAnimation.ts   # 滚动动画 Hook（IntersectionObserver）
├── App.vue                     # 根组件
├── main.ts                     # 应用入口
└── vite-env.d.ts               # 类型声明
```

---

## 🚀 快速开始 | Getting Started

### 环境要求 | Prerequisites

- Node.js >= 18.0
- npm >= 9.0

### 安装与运行 | Install & Run

```bash
# 克隆仓库
git clone https://github.com/Z9-Studio/ai-leadership-course.git

# 进入项目目录
cd ai-leadership-course

# 安装依赖
npm install

# 启动开发服务器
npm run dev
```

### 构建生产版本 | Production Build

```bash
npm run build
```

构建产物输出到 `dist/` 目录，可部署至任意静态托管服务。

---

## 📄 页面板块 | Page Sections

| 序号 | 板块 | 描述 |
|------|------|------|
| 1 | 导航栏 | 固定顶部，锚点导航，移动端汉堡菜单 |
| 2 | Hero Banner | 核心口号 + CTA 按钮 + 动态背景 |
| 3 | 核心优势 | 20年+ 经验 / 50亿+ 项目额 / 8大 认证 / 100+ 企业 |
| 4 | 课程体系 | 企业 / 高校 / 青少年三大"1+3+X"课程体系 |
| 5 | 讲师介绍 | 头像、头衔矩阵、社会职务、著作展示 |
| 6 | 授课风格 | 理论+实战 / 国际视野 / 案例驱动 / 启发互动 |
| 7 | 案例展示 | 企业 LOGO 墙 + 典型案例卡片 |
| 8 | 课程视频 | 视频卡片列表（可扩展） |
| 9 | 合作咨询 | 联系方式 + 预约咨询 |
| 10 | 页脚 | 品牌信息 + 快速导航 |

---

## 🎨 设计规范 | Design Specification

| 项目 | 值 |
|------|------|
| 主色 | `#0052D9`（科技蓝） |
| 辅助色 | `#E8A838`（金色点缀） |
| 背景色 | `#FFFFFF` / `#F5F7FA` |
| 深色背景 | `#0A1628` |
| 正文字体 | 系统无衬线字体栈 |
| 圆角 | `8px` / `12px` / `16px` |
| 最大内容宽度 | `1200px` |

---

## 📝 关于刘言午 | About Liu Yanwu

刘言午，管理学者、作家，智午研究院（since 2010）院长。亚太数字经济学会常务理事长，中国技术经济学会高级委员，中国电子信息行业联合会数字经济专委会 AI 大模型工作组负责人。

**代表著作：**
- 《AI领导力》（2024，中国科学技术出版社）
- 《决胜数字化转型》（2025，中国科学技术出版社）

**服务客户：** 中国建材、中国再保险、中国移动、中国联通、中国电信、新浪、360集团、比亚迪等多家政府及500强企业。

Liu Yanwu is a management scholar, author, and Director of Zhiwu Research Institute (est. 2010). He serves as Executive Vice Chairman of the Asia-Pacific Digital Economy Society and holds multiple national-level academic appointments.

**Publications:** *"AI Leadership"* (2024), *"Winning Digital Transformation"* (2025)

**Clients:** China National Building Material, China Reinsurance, China Mobile, China Unicom, China Telecom, Sina, Qihoo 360, BYD, and numerous Fortune 500 enterprises.

---

## 📜 版本历史 | Version History

### [v0.0.1](https://github.com/Z9-Studio/ai-leadership-course/releases/tag/v0.0.1) — 初始版本

- 完整落地页 10 大板块实现
- Vue 3 + TDesign + Tailwind CSS 技术栈集成
- 响应式布局适配
- 滚动淡入动画
- 课程体系 Tab 交互

---

## 📄 开源协议 | License

[MIT License](LICENSE) © 2025 Z9 Studio

---

## 🤝 联系方式 | Contact

如有课程咨询或合作需求，请通过网站底部联系方式与我们取得联系。

For course inquiries or collaboration opportunities, please use the contact information provided at the footer of the website.
