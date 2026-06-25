<template>
  <div class="home_page">
    <div class="start">
      <div class="start-item1">
        <div class="small-title">
          赋能新一代生产级智能体，释放智能生产力
          <img src="@/assets/VLimg2.0/small-title.png" alt="" />
        </div>
      </div>
      <div class="start-item2">
        <img src="@/assets/VLimg2.0/title.png" alt="" />
      </div>
      <div class="start-item3">
        打造稳定可靠、可复用、可扩展的生产级智能体，满足多元业务场景需求
      </div>
      <div class="start-item4">
        <div class="buttom1">
          立即试用
        </div>
        <div class="buttom2">
          安排演示
        </div>
      </div>
      <div ref="imageContainer" class="start-item5">
        <img
          ref="animatedImage"
          src="@/assets/VLimg2.0/start-img1.png"
          alt=""
          class="scroll-3d-image"
          :class="{ 'tilted': isImageTilted }"
        />
      </div>
    </div>
    <div class="main-content">
      <div class="w1440 box">
        <div class="title">
          OortCloud Super AI Agent 平台
        </div>
        <div class="deputy-title">
          贯通功能开发-工程化落地-企业应用-数据闭环，支持深度定制开发的企业级Agent开发平台
        </div>
        <div class="item-list">
          <div class="item">
            <img src="@/assets/VLimg2.0/item-img1.png" alt="" />
            <div class="item-title">
              Chat Bot 机器人
            </div>
            <div class="item-content">
              依托人工智能技术，它专注基础人机交互，为场景提供便捷智能对话能力
            </div>
          </div>
          <div class="item">
            <img src="@/assets/VLimg2.0/item-img2.png" alt="" />
            <div class="item-title">
              丰富的 AI 智能体
            </div>
            <div class="item-content">
              多样化 AI 智能体深度协同，构建高效智能体系，赋能数字化场景应用
            </div>
          </div>
          <div class="item">
            <img src="@/assets/VLimg2.0/item-img3.png" alt="" />
            <div class="item-title">
              语音与虚拟人智能体
            </div>
            <div class="item-content">
              原生支持语音、虚拟人、声音复刻、角色人格化开发，构建有温度的智能体
            </div>
          </div>
          <div class="item">
            <img src="@/assets/VLimg2.0/item-img4.png" alt="" />
            <div class="item-title">
              多范式一站式Agent开发能力
            </div>
            <div class="item-content">
              支持 Prompt / Workflow / Agentic Workflow，全流程闭环开发与优化
            </div>
          </div>
          <div class="item">
            <img src="@/assets/VLimg2.0/item-img5.png" alt="" />
            <div class="item-title">
              智能RPA 跨系统协同
            </div>
            <div class="item-content">
              多样化 AI 智能体深度协同，构建高效智能体系，赋能数字化场景应用
            </div>
          </div>
          <div class="item">
            <img src="@/assets/VLimg2.0/item-img6.png" alt="" />
            <div class="item-title">
              企业级管理与运营
            </div>
            <div class="item-content">
              支持团队空间、权限分级与效果闭环，助力智能体从开发到持续优化
            </div>
          </div>
        </div>
      </div>
      <div class="w1440 box">
        <div class="title">
          开放生态，连接智能体的无限可能
        </div>
        <div class="deputy-title">
          让每个能力都能被快速接入、复用与共享，让智能体开发真正具备可组合、可扩展的生产力
        </div>
        <div class="w1440 privateBox">
          <div class="flexRowAC w1440 colMenu">
            <div class="left-menu">
              <div
                v-for="(item, index) in superItems"
                :key="index"
                class="menu-item"
                :class="{ active: activeIndexSuper === index }"
                @click="selectMenu(index)"
              >
                <div class="menu-content-wrapper">
                  <div class="line" />
                  <div class="text-content">
                    <div class="menu-text">
                      {{ item.title }}
                    </div>
                    <div v-show="activeIndexSuper === index" class="content-detail">
                      <p>{{ currentSuper.description }}</p>
                    </div>
                  </div>
                </div>
              </div>
            </div>
            <div class="right-content">
              <div>
                <img :src="currentSuper.image" :alt="currentSuper.title" class="content-image" />
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="w1440 box">
        <div class="title" style="text-align: center;">
          共建新一代智能体
        </div>
        <div class="deputy-title" style="text-align: center;">
          企业级、商业友好型智能工作流平台，开源共建新一代超级智能体
        </div>
        <div class="productImg product1">
          <img class="pro1_1" src="@/assets/VLimg2.0/down1.png" alt="" />
          <div class="pro1_1_s flexRowAC">
            OortCloud Super AI Agent
          </div>
          <div class="pro1_2 flexRowAC">
            <img class="pro1_2_i" src="@/assets/VLimg2.0/down2.png" alt="" />
            Accelerate Agentic AI
          </div>
          <div class="pro1_2 flexRowAC">
            <img class="pro1_2_i" src="@/assets/VLimg2.0/down2.png" alt="" />
            Strengthen Productivity
          </div>
          <div class="pro1_2 flexRowAC">
            <img class="pro1_2_i" src="@/assets/VLimg2.0/down2.png" alt="" />
            Onspire Imagination
          </div>
          <div class="pro3 flexRowAC">
            <!-- <NuxtLink
            to="/zh/demoGA"
            target="_blank"
          >
            <div class="pro3_btn flexRowAC">
              试用
            </div>
          </NuxtLink> -->
            <div class="pro3_btn flexRowAC">
              立即体验
            </div>

            <div class="pro3_btn p3b flexRowAC">
              前往 GitHub
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref, computed, onMounted, onUnmounted } from 'vue'
// import { useScroll } from '@vueuse/core'
import menu_img1 from '@/assets/VLimg2.0/menu-img1.png'
import menu_img2 from '@/assets/VLimg2.0/menu-img2.png'
import menu_img3 from '@/assets/VLimg2.0/menu-img3.png'
import menu_img4 from '@/assets/VLimg2.0/menu-img4.png'

const superItems = ref([
  {
    title: '多渠道一键发布',
    description: '支持 Workup APP、网页端、桌面端、小程序、API 等多端触达，实现智能体从开发到上线的"零门槛"分发与快速验证',
    image: menu_img1
  },
  {
    title: '多领域模版与行业方案',
    description: '支持多领域模板与行业方案，实现智能体从开发到上线的"零门槛"分发与快速验证',
    image: menu_img2
  },
  {
    title: '能力托管与 API 导流机制',
    description: '支持智能体方案上架 OORT 开放平台生态，通过能力托管与API导流，让智能体快速复用、规模化推广',
    image: menu_img3
  },
  {
    title: '迈向多智能体的 Super AI Agent时代',
    description: '每个智能体都能成为生态中的节点，既贡献价值，也共享增长共同构建一个开放、可循环、可演化的Super AI Agent生态',
    image: menu_img4
  }
])

const activeIndexSuper = ref(0)
const currentSuper = computed(() => {
  return superItems.value[activeIndexSuper.value]
})
function selectMenu(index) {
  activeIndexSuper.value = index
}

const animatedImage = ref(null)
const imageContainer = ref(null)
const isImageTilted = ref(true) // 标记是否已倾斜
// const { y: scrollY } = useScroll() // 滚动Y轴距离

// 滚动触发函数：判断阈值
function handleScroll() {
  if (!imageContainer.value) return

  // 获取容器位置和滚动距离
  const containerRect = imageContainer.value.getBoundingClientRect()
  // 当图片顶部距离视口顶部 < 200px 时
  const triggerThreshold = 200

  // 2. 逻辑反转：滚动到阈值时取消倾斜，回滚时恢复倾斜
  // 满足条件则取消倾斜
  if (containerRect.top < triggerThreshold && isImageTilted.value) {
    isImageTilted.value = false
  }
  // 回滚时恢复倾斜
  if (containerRect.top > triggerThreshold + 100 && !isImageTilted.value) {
    isImageTilted.value = true
  }
}

onMounted(() => {
  window.addEventListener('scroll', handleScroll, { passive: true })
})

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll)
})

</script>

<style scoped lang="less">
@import "src/assets/style/vars.less";

.home_page{
  background-color: #fff;
}

.w1440{
  width: 1440px;
  margin: 0 auto;
}
.box{
  padding-bottom: 160px;
}
.start{
  height: 1457px;
  background: url(@/assets/VLimg2.0/bg.png);
  background-repeat: no-repeat;
  background-size: cover;
  display: flex;
  flex-direction: column;
  align-items: center;
  perspective: 1000px;
  perspective-origin: center center;
  margin-bottom: 120px;
}

.small-title{
  display: flex;
  align-items: center;
  background-color: #fff;
  width: fit-content;
  font-size: 16px;
  border-radius: 445px;
  gap: 5px;
  padding: 10px 20px;
  img{
    width: 24px;
    height: 24px;
  }
}

.title{
  font-size: 50px;
  font-weight: 700;
  margin-bottom: 20px;
}
.deputy-title{
  font-size: 20px;
  color: #717781;
  margin-bottom: 80px;
}

.item-list{
  display: flex;
  gap: 20px;
  flex-wrap: wrap;
  .item{
    width: 466px;
    padding-bottom: 24px;
    text-align: center;
    img{
      width: 466px;
      height: 206px;
      margin-bottom: 24px;
    }
    .item-title{
      font-size: 24px;
      color: #333;
      font-weight: 600;
      margin-bottom: 14px;
    }
    .item-content{
      font-size: 18px;
      color: #333333;
      padding: 0 36px;
    }
  }
}
.colMenu{
  justify-content: space-between;
  // margin-bottom: 160px;
}

.left-menu {
  width: 470px;
  display: flex;
  flex-direction: column;
  gap: 32px;
  margin-right: 16px;

  .menu-item {
    position: relative;
    cursor: pointer;

    &:last-child {
      border-bottom: none;
    }

    &.active {
      .menu-text {
        color: #333333;
        font-size: 46px;
        line-height: 82px;
      }
    }

    .menu-content-wrapper {
      display: flex;
      gap: 16px;
      position: relative;
    }

    .line {
      position: absolute;
      left: -24px;
      top: 0;
      width: 6px;
      height: 48px;
      background-color: #E8EAED;
      transition: height 0.4s cubic-bezier(0.4, 0, 0.2, 1);
      border-radius: 33px;
    }

    &.active .line {
      height: 100%;
      background-color: #2E63FF;
    }

    .text-content {
      flex: 1;
    }

    .menu-text {
      transition: all 0.3s ease;
      color: #666666;
      font-weight: bold;
      font-size: 32px;
      line-height: 48px;
    }

    .content-detail {
      p {
        color: #717781;
        font-size: 20px;
        line-height: 30px;
        margin-top: 20px;
      }
    }
  }
}

.content-image{
  width: 860px;
  height: 568px;
}

.product1 {
  margin: 0 auto;
  text-align: left;
  color: #fff;
  width: 100%;
  height: 510px;
  background-color: #fff;
  border-radius: 24px;
  background: linear-gradient(135deg, #0C1F40 0%, #252734 98%);
  padding: 40px;

  .pro1_1 {
    width: 60px;
    height: 60px;
    margin-bottom: 40px;
  }

  .pro1_1_s {
    padding-bottom: 40px;
    gap: 12px;
    color: #FFFFFF;
    font-weight: bold;
    font-size: 24px;

    .pro1_1_s_b {
      color: #FFFFFF;
      font-size: 14px;
      border-radius: 4px;
      border: 0.5px solid #FFFFFF;
      padding: 4px 10px;
    }
  }

  .pro1_2 {
    gap: 12px;
    padding-bottom: 24px;

    .pro1_2_i {
      width: 16px;
      height: 16px;
    }
  }

  .pro3 {
    padding-top: 35px;
    gap: 30px;

    .pro3_btn {
      flex: 1;
      padding: 20px 0;
      justify-content: center;
      background-color: #fff;
      border-radius: 4px;
      color: #333;
      font-weight: bold;
      font-size: 18px;
    }

    .pro3_btn.p3b {
      background-color: transparent;
      border: 1px solid #fff;
      color: #fff;
    }
  }
}
.start-item1{
  margin-top: 120px;
}
.start-item2{
  margin: 40px 0;
  img{
    width: 1133px;
    height: 83px;
  }
}
.start-item3{
  font-size: 24px;
  font-weight: 600;
  margin-bottom: 60px;
}
.start-item4{
  font-size: 18px;
  font-weight: 700;
  display: flex;
  justify-content: center;
  gap: 20px;
  margin-bottom: 80px;
}
.buttom1,.buttom2{
  padding: 20px 48px;
  border-radius: 8px;
}
.buttom1{
  background-color: #2278FF;
  color: #fff;
}
.buttom2{
  background-color: #fff;
  color: #333;
}
.start-item5{
  transform-style: preserve-3d;
  img{
    width: 1300px;
    height: 885px;
    // 初始平面状态
    transform: rotateX(0deg) scale(1) translateY(0);
    transform-style: preserve-3d;
    backfaceVisibility: hidden;
    // 倾斜过渡动画（控制倾斜速度）
    transition: transform 0.5s cubic-bezier(0.4, 0, 0.2, 1);
    will-change: transform;
  }
}

.scroll-3d-image.tilted {
  transform: rotateX(20deg) scale(1.02) translateY(-50px) !important;
  // 可自定义倾斜参数：
  // rotateX：向内倾斜角度（正数=上边缘向内，负数=下边缘向内）
  // scale：轻微缩放增强视觉效果
  // translateY：轻微位移配合倾斜
}
</style>
