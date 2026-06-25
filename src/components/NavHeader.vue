<template>
  <div class="nav flexRowAC" :class="{navFixed:isSticky}">
    <div class="navImg">
      <img v-if="isActPath.includes('vlsIndex')" class="navLogo" src="@/assets/VLimg2.0/OORT.AI.png" alt="" />
      <img v-else class="navLogo" src="@/assets/VLimg2.0/OORT.AI.png" alt="" />
      <span>OORT.AI</span>
    </div>
    <div class="flexRowAC nav_t">
      <div
        v-for="(item,i) in navList"
        :key="i"
        class="nav_title"
        :class="{nav_t_line:isActPath===item.path&&(item.title.includes(propTemp) || i>2)}"
        @click="navClick(item.path,item.title)"
      >
        {{ item.title }}
      </div>
    </div>
    <div class="flexRowAC nav_r">
      <NuxtLink to="http://oort.oortcloudsmart.com:23410/bus/apaas-web/console_manage/index.html" target="_blank">
        <div class="login_but">
          <span>登录/注册</span>
        </div>
      </NuxtLink>
      <el-popover placement="bottom" trigger="click" popper-class="popover_panel">
        <template #reference>
          <img class="right_info_nine" src="@/assets/navheader/nightpointpng.png" />
        </template>
        <commonRightPoPover @more-opr="moreOpr" />
      </el-popover>
    </div>
  </div>
</template>

<script setup>
import { ref, defineEmits, computed, watch } from 'vue'
import { useRouter, useRoute } from 'vue-router'
import commonRightPoPover from './commonRightPoPover.vue'

const prop = defineProps(['item', 'sel', 'isSticky'])
const propTemp = ref(prop.item)
const router = useRouter()
const route = useRoute()
const isActPath = computed(() => {
  let routePath = route.path
  if (route.path === '/serviceExtend') {
    routePath = '/service'
  }
  if (route.path === '/productworkUp' || route.path === '/productxoa' || route.path === '/productaPaas' || route.path === '/productmPaas') {
    routePath = '/product'
  }
  return routePath
})
const emit = defineEmits(['handle'])
const navList = ref([
  { title: '应用程序', path: '/zh' },
  { title: '行业', path: '/zh' },
  { title: '社区', path: '/zh' },
  { title: '定价', path: '/zh/price' },
  { title: '联系方式', path: '/zh/contactUs' }
])

const navClick = (path, t) => {
  emit('handle', t)
  router.push(path)
}

watch(() => prop.item, (newVal) => {
  propTemp.value = newVal
}, { immediate: true })

</script>

<style>

.popover_panel {
  width: 400px!important;
  background-color: #EDF3F9!important;
  border-radius: 10px!important;
}

.popover_panel .el-popper__arrow:before {
  background-color: #EDF3F9!important;
}

</style>

<style lang="scss" scoped>

.login_but:hover {
  background-color: #1066ef;
}
.login_but {
  cursor: pointer;
  width: 132px;
  height: 44px;
  margin: 0 10px;
  border-radius: 2px;
  background-color: #2278FF;
  display: flex;
  align-items: center;
  justify-content: center;
  span {
    font-weight: 400;
    font-size: 18px;
    color: #FFFFFF;
    line-height: 24px;
    letter-spacing: 1px;
  }
}

.right_info_nine {
  width: 46px;
  height: 46px;
  margin: 0 12px;
  cursor: pointer;
  border-radius: 0;
  transition: border-radius 0.5s ease; /* 添加过渡效果 */
}

.right_info_nine:hover {
  border-radius: 50%;
}

:deep(.el-tooltip__trigger:focus-visible) {
  outline: unset;
}

.langBox {
  cursor: pointer;
  margin-left: 20px;
  background: rgba(216, 216, 216, 0.00);
  padding: 12px;
  border: 0.6px solid #333;

  .langBoxT {
    font-size: 14px;
    color: #333;
  }

  img.demo_img {
    width: 16px;
    height: 16px;
  }
}
.navFixed{
  position: fixed;
  left: 0;
  top: 0;
  right: 0;
  width: 100%;
  height: 82px;
  z-index: 10;
}

.nav_title::after {
  content: "";
  display: block;
  position: relative;
  width: 36px;
  margin: auto;
  top: 10px;
  border-bottom: 4px solid transparent;
}

.nav_t_line {
  color: #EB691C;
}

.nav_t_line::after {
  border-bottom: 4px solid #EB691C;
}

.nav {
  width: 100%;
  color: #5C5C5C;
  height: 82px;
  justify-content: space-between;
  padding: 0 220px;
  box-shadow: 0px 0px 4px 2px #DADADA;
  background-color: #fff;
  .nav_t {
    cursor: pointer;
    gap: 28px;
    font-size: 18px;
    color: #5C5C5C;
    font-weight: 700;
  }

  .navImg {
    width: 200px;
    display: flex;
    align-items: center;
    span{
      margin-left: 10px;
      font-size: 24px;
      font-weight: 900;
      color: #2278FF;
    }
  }

  .nav_r {
    justify-content: end;
    width: 200px;
  }

  .navLogo {
    height: 48px;
    background-size: cover;
  }

  .demo_img {
    width: 24px;
    height: 24px;
    background-size: cover;
    margin-right: 8px;
  }
}

:deep(.el-dialog){
  padding: 0;

  .el-dialog__header{
    padding: 0;
  }
}
</style>
