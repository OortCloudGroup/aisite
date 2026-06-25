<template>
  <div class="home_page vls">
    <div class="platTop w1380">
      <div class="VLStream flexRowAC">
        奥尔特云
        <div class="empoPlat">
          数据赋能
        </div>
        平台
      </div>
      <div class="plat_d">
        面向 <span style="color: #2278FF" class="ai_time">AI时代
          <img src="@/assets/img/ai.png" alt="" class="ai_picture" />
        </span> 的新型数据底座
      </div>
      <div class="flexRowAC useBox">
        <div class="seeMore">
          立即试用
        </div>
        <div class="seeMore u1">
          安排演示
        </div>
      </div>
    </div>
    <div class="w1380 CloudBox flexRowAC">
      <div class="CloudL">
        <div class="cl_t">
          数据汇聚管理
        </div>
        <div class="cl_d">
          支持数据源配置管理、库表集成、文件集成、API集成等功能，帮助实现高效数据整合与统一管理。
        </div>
      </div>
      <img class="k8sMana_c1" src="@/assets/software/empoPlat_c1.png" alt="" />
    </div>
    <div class="w1380 CloudBox ipcBox flexRowAC">
      <img class="k8sMana_c1" src="@/assets/software/empoPlat_c2.png" alt="" />
      <div class="CloudL">
        <div class="cl_t">
          数据综合治理
        </div>
        <div class="cl_d">
          提供数据清洗、分类管理、元数据管理、标准管理与质量管理功能，实现数据全生命周期规范化治理。
        </div>
      </div>
    </div>
    <div class="w1380 ipcView CloudBox flexRowAC">
      <div class="CloudL">
        <div class="cl_t">
          数据仓库管理
        </div>
        <div class="cl_d">
          提供数仓管理、数据操作服务、数据安全管理与数据资产管理功能，助力高效、安全的数据存储与应用。
        </div>
      </div>
      <img class="k8sMana_c1" src="@/assets/software/empoPlat_c3.png" alt="" />
    </div>
    <div class="w1380 ipcView CloudBox flexRowAC">
      <img class="k8sMana_c1" src="@/assets/software/empoPlat_c4.png" alt="" />
      <div class="CloudL" style="text-align: right">
        <div class="cl_t">
          知识图谱管理
        </div>
        <div class="cl_d">
          支持本体模型管理、知识管理、图谱构建与关联分析，实现智能化知识组织与深度关联挖掘。
        </div>
      </div>
    </div>
    <div class="w1380 CloudBox flexRowAC">
      <div class="CloudL">
        <div class="cl_t">
          数据开放管理
        </div>
        <div class="cl_d">
          提供数据服务总览、服务目录管理、API管理、服务审批、数据集市及精准推送功能，全面提升数据共享与服务效率。
        </div>
      </div>
      <img class="k8sMana_c1" src="@/assets/software/empoPlat_c5.png" alt="" />
    </div>
    <div class="w1380 CloudBox flexRowAC">
      <img class="k8sMana_c1" src="@/assets/software/empoPlat_c51.png" alt="" />
      <div class="CloudL" style="text-align: right">
        <div class="cl_t">
          大模型智能平台
        </div>
        <div class="cl_d">
          支持教学助手创建、场景交互、资源分析、语音提问、对话管理与专业知识问答，助力智能化教学与知识管理
        </div>
      </div>
    </div>
    <div class="w1380 CloudBox flexRowAC">
      <div class="CloudL">
        <div class="cl_t">
          知识图谱智能应用
        </div>
        <div class="cl_d">
          专业增养方案阳形化展示、课程推荐、学习路径规划、能分析及课程导航，助力教育资源优化与智能决策，
        </div>
      </div>
      <img class="k8sMana_c1" src="@/assets/software/empoPlat_c6.png" alt="" />
    </div>
    <div class="w1380 CloudBox flexRowAC">
      <img class="k8sMana_c1" src="@/assets/software/empoPlat_c7.png" alt="" />
      <div class="CloudL" style="text-align: right">
        <div class="cl_t">
          技术实施服务
        </div>
        <div class="cl_d">
          提俱数据仓库规划、数据治理、数据对接及课程、专业、人才培养方案知识能语构建服务，推式效据与知识的深度融合应用。
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
</script>

<style scoped lang="less">
@import "src/assets/style/vars.less";

.home_page {
  position: relative;
}

.home_page.vls {
  background-color: #fff;
}

.w1380 {
  width: 1380px;
  margin: 0 auto;
}

// 查看更多
//.seeMore {
//  display: inline-block;
//  padding: 24px 50px;
//  color: #fff;
//  border: 1px solid #2278FF;
//  border-radius: 8px;
//  background: #2278FF;
//  box-shadow: 0px 4px 10px 0px #FF5E1033;
//  font-weight: bold;
//  font-size: 18px;
//}

.platTop {
  text-align: center;
  padding: 110px 0;

  .plat {
    display: inline-block;
    padding: 12px 24px;
    color: #FF5E10;
    font-size: 18px;
    border-radius: 18px;
    border: 1px solid #E9E9E9;
  }

  .VLStream {
    justify-content: flex-start;
    color: #333333;
    font-weight: bold;
    font-size: 78px;
    padding: 8px 0 0 0;
    position: relative;

    .VLStream_img {
      width: 222px;
      height: 222px;
      position: absolute;
      right: 336px;
      top: -50px;
    }
    .empoPlat{
      background-image: url("@/assets/software/empoPlat.png");
      background-size: 100% 100%;
      padding: 4px 12px;
      line-height: 110px;
    }
  }

  .plat_d {
    display: flex;
    color: #333333;
    font-weight: bold;
    font-size: 78px;
    text-align: left;
    padding-top: 20px;
    padding-bottom: 80px;

    .ai_time{
      display: flex;
      flex-direction: column;
      align-items: center;
      margin: 0 5px;

      .ai_picture{
        width: 276px;
        height: 16px;
      }
    }

  }

  .plat_a {
    color: #333333;
    font-weight: bold;
    font-size: 58px;
  }

  .plat_cent {
    padding: 20px 0 50px;
    color: #717781;
    font-size: 18px;
  }

  .useBox {
    justify-content: center;
    gap: 20px;

    .seeMore {
      padding: 24px 50px;
      color: #fff;
      border: 1px solid #2278FF;
      border-radius: 8px;
      background: #2278FF;
      //box-shadow: 0px 4px 10px 0px #FF5E1033;
      font-weight: bold;
      font-size: 18px;
    }

    .u1 {
      color: #333;
      background-color: #F4F4F4;
      border: 1px solid #F4F4F4;
    }

    .seeMore.u2 {
      display: flex;
      gap: 10px;
      border: 1px solid #333;
      background-color: #333;

      .u2_img {
        width: 28px;
        height: 26px;
      }
    }
  }
}

.WebRTC {
  gap: 24px;
  padding-bottom: 80px;
  animation: scroll 35s linear infinite;

  .webItem {
    width: auto;
    height: 120px;
    border-radius: 16px;
    background: #E8F7FC;
    color: #5C6C00;
    gap: 14px;
    flex-wrap: nowrap;
  }
}

@keyframes scroll {
  0% {
    transform: translateX(0%);
  }
  100% {
    transform: translateX(-100%);
  }
}

.webBottomImg {
  padding: 70px 0 110px;
  height: initial;

  .wBImg {
    width: 100%;
    height: initial;
    border-radius: 24px;
  }
}

.CloudBox {
  padding-bottom: 100px;
  justify-content: space-between;
  align-items: flex-start;

  .cl_t {
    letter-spacing: 0;
    padding-top: 30px;
    padding-bottom: 40px;
    color: #3D3D3D;
    font-weight: bold;
    font-size: 54px;
  }

  .cl_d {
    padding-bottom: 24px;
    color: #717781;
    font-size: 20px;
  }

  .CloudL {
    width: 500px;
  }

  .CloudR {
    width: 700px;
    height: auto;

    .CloudRImg {
      width: 100%;
      height: 100%;
    }
  }

  .CloudR2 {
    width: 700px;
    height: 700px;
  }
}

.ipcBox.CloudBox {
  padding-bottom: 120px;
  justify-content: space-between;
  align-items: flex-start;

  .CloudL {
    width: 450px;
    text-align: right;
    padding-top: 60px;
  }
}

.ipcView.CloudBox {
  .CloudR {
    height: 460px;
  }
}

.productBox {
  text-align: center;
  padding-bottom: 140px;

  .proT {
    padding-bottom: 60px;
    color: #3D3D3D;
    font-weight: bold;
    font-size: 58px;
  }

  .prod {
    padding-bottom: 60px;
    color: #717781;
    font-size: 20px;
  }

  .productImg {
    width: 100%;
    height: 600px;
    padding-bottom: 60px;

    .proImg {
      width: 100%;
      height: 100%;
    }
  }

  .product1 {
    text-align: left;
    color: #fff;
    width: auto;
    height: 510px;
    background-color: #fff;
    border-radius: 24px;
    background: linear-gradient(135deg, #0C1F40 0%, #252734 98%);
    padding: 40px;

    .pro1_1 {
      width: 46px;
      height: 48px;
      margin-bottom: 46px;
    }

    .pro1_1_s {
      padding-bottom: 50px;
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
      padding-bottom: 30px;

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

  .product2Out {
    padding-bottom: 0;
    height: 220px;
    justify-content: center;
    background-image: url('@/assets/software/downloadBG.png');
    background-size: 100% 100%;

    .product2Out_it {
      opacity: 1;
      color: #333333;
      font-size: 16px;

      .pro2o_l {
        padding-left: 12px;
        width: 600px;
        height: 54px;
        background-color: #F0F0F0;

        .pro2o_l_l {
          width: 34px;
          height: 34px;
          margin-right: 12px;
        }
      }

      .pro2o_2 {
        width: 100px;
        line-height: 54px;
        color: #fff;
        height: 54px;
        background-color: #2278FF;
      }
    }
  }

  .product3Out.productImg {
    height: initial;
    margin-bottom: 60px;
    padding: 40px;
    border-radius: 24px;
    background: linear-gradient(180deg, #FEF9F6 0%, #FFFFFF 100%);
    border: 1px solid #001F5019;

    .p3Box {
      justify-content: space-between;

      .p3 {
        width: 358px;
        height: 170px;
      }
    }

    .p3_title {
      padding-top: 40px;
      text-align: left;
      color: #3D3D3D;
      font-weight: bold;
      font-size: 24px;
    }

    .ps_desc {
      padding-top: 16px;
      padding-left: 60px;
      width: 900px;
      color: #3D3D3D;
      font-size: 20px;
      text-align: left;
      position: relative;

      &::before {
        content: '';
        position: absolute;
        left: 40px;
        top: 26px;
        width: 8px;
        height: 8px;
        border-radius: 50%;
        background-color: #333;
      }
    }
  }

  .p4Out {
    width: auto;
    height: 870px;
  }

  .p5Out {
    flex-wrap: wrap;
    gap: 40px;

    .p5Item {
      padding: 50px 0;
      flex-direction: column;
      border-radius: 40px;
      background: #FFFFFF;
      box-shadow: 0px 0px 48px 0px #07005714;
      width: 300px;
      height: 300px;
      flex-shrink: 0;
      gap: 10px;
      position: relative;
    }

    .p5Iimg {
      width: 110px;
      height: 110px;
    }

    .p5t {
      color: #3D3D3D;
      font-weight: bold;
      font-size: 24px;
    }

    .p5d {
      color: #717781;
      font-size: 14px;
    }

    .proCode {
      width: 70px;
      height: 70px;
      position: absolute;
      right: 0;
      top: 0;
      border-radius: 0px 0px 0px 0px;
    }
  }
}

.k8sMana_c1{
  width: 692px;
  height: auto;
}
</style>
