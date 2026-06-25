# OORT.AI 企业官网

<p align="center">
  <strong>面向企业级 AI Agent、数字化应用与智能物联网场景的品牌官网项目</strong>
</p>

<p align="center">
  <img alt="Nuxt" src="https://img.shields.io/badge/Nuxt-3.15-00DC82?style=flat-square&logo=nuxtdotjs" />
  <img alt="Vue" src="https://img.shields.io/badge/Vue-3-4FC08D?style=flat-square&logo=vuedotjs" />
  <img alt="Element Plus" src="https://img.shields.io/badge/Element%20Plus-Nuxt-409EFF?style=flat-square" />
  <img alt="License" src="https://img.shields.io/badge/License-Apache--2.0-blue?style=flat-square" />
</p>


<p align="center">
  <img src="./src/assets/VLimg2.0/start-img1.png" alt="OORT.AI 首页主视觉" width="860" />
</p>

<p align="center">
  <img src="./src/assets/VLimg2.0/menu-img1.png" alt="多渠道一键发布" width="420" />
  <img src="./src/assets/VLimg2.0/menu-img3.png" alt="能力托管与 API 导流机制" width="420" />
</p>

## 项目简介

这是一个基于 Nuxt 3 构建的企业官网项目，围绕 OORT.AI / OortCloud 的产品、平台能力、行业方案、价格计划与联系入口进行展示。

网站首页重点呈现 `OortCloud Super AI Agent` 平台，强调生产级智能体开发、工程化落地、企业应用、数据闭环与开放生态能力。站点同时覆盖应用市场、行业场景、定价方案、社区资源与企业联系信息，适合作为公司官网、产品展示页、开源官网模板继续迭代。

## 网站内容

| 页面 | 内容 |
| --- | --- |
| 首页 | 展示 Super AI Agent 平台、智能体能力、开放生态、多渠道发布与 GitHub 入口 |
| 应用程序 | 展示个人效率、培训学习、指挥调度、行政后勤、生产力工具、业务管理、队伍建设、IOT 等应用类别 |
| 行业 | 覆盖物业、园区、街道、消防、律所、停车、酒厂等行业入口，以及销售、客服、研发、数据分析、HR、财务等职能场景 |
| 定价 | 提供免费、标准、定制等服务计划，展示 OortCloud Online、OortCloud.sh、离线版与定制服务能力 |
| 联系我们 | 提供在线留言、电话、邮箱、公司地址与产品咨询入口 |
| 社区 | 包含文档、客户案例、合作伙伴、近期活动、隐私、安全、支持等内容模块 |

## 核心亮点

- 企业级 AI Agent 官网首页，突出智能体开发、工作流、RPA、虚拟人和运营管理能力。
- 多栏目产品展示，覆盖应用、行业、职能、场景与 IOT 方向。
- 清晰的价格页，支持年缴/月缴切换和不同服务计划展示。
- 完整的联系页，包含表单、直联方式与企业地址信息。
- 桌面端与移动端布局拆分，适配不同访问场景。
- 使用 Nuxt 3、Vue 3、Element Plus、Pinia、VueUse、Swiper、Less / Sass 构建。

## 技术栈

| 分类 | 技术 |
| --- | --- |
| 框架 | Nuxt 3、Vue 3 |
| 状态管理 | Pinia |
| UI 组件 | Element Plus |
| 工具库 | VueUse、lodash-es、date-fns、axios |
| 样式 | CSS、Less、Sass、postcss-px-to-viewport |
| 交互 | Swiper、fullpage.js |
| 工程化 | ESLint、Husky、Commitlint |

## 目录结构

```text
src
├─ api                 # 接口请求模块
├─ assets              # 图片、样式、官网视觉资源
├─ components          # 通用导航、底部、弹层等组件
├─ composables         # 组合式逻辑
├─ config              # 项目配置
├─ lang                # 中英文文案
├─ layouts             # 页面布局
├─ pages               # Nuxt 页面路由
├─ plugins             # 插件注册
├─ public              # 静态资源
├─ stores              # Pinia 状态
└─ utils               # 通用工具函数
```

## 快速开始

推荐使用 `pnpm` 安装依赖。

```bash
pnpm install
```

启动本地开发服务：

```bash
pnpm start
```

默认访问地址：

```text
http://localhost:8080
```

## 常用命令

| 命令 | 说明 |
| --- | --- |
| `pnpm start` | 启动 Nuxt 开发服务 |
| `pnpm build` | 构建生产环境产物 |
| `pnpm generate` | 生成静态站点 |
| `pnpm preview` | 本地预览生产构建 |
| `pnpm lint` | 执行 ESLint 修复 |

## 部署说明

项目支持 Nuxt 构建与静态生成。当前 README 推荐静态站点部署流程：

```bash
pnpm generate
```

生成后的静态资源可交由 Nginx、对象存储、CDN 或任意静态站点服务托管。

Nginx 示例：

```nginx
server {
  listen 80;
  server_name example.com;

  root /path/to/project/.output/public;
  index index.html;

  location / {
    try_files $uri $uri/ /index.html;
  }
}
```

## 开源协作

欢迎基于本项目继续完善官网内容、视觉资源、响应式体验与国际化文案。

提交信息请遵循 Conventional Commits：

```text
feat: 新增官网页面模块
fix: 修复移动端布局问题
docs: 更新项目说明文档
style: 调整页面样式
refactor: 优化组件结构
```

## 待完善

- 补充线上预览地址。
- 清理历史模板文案，统一品牌表述。
- 完善移动端页面和多语言文案。

## 许可证

本项目基于 Apache License 2.0 开源，详情请查看 [LICENSE](./LICENSE)。
