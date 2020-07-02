<template>
    <div id="Software">
        <!-- <div class="row">
            <div id="left" class="col-md-4 col-xs-12">
                <ul class="left-container wow bounceInLeft">
                    <p>软件产品</p>
                    <li v-for="(item,index) in softwareList" :key="index">
                        <router-link :to=item.path>{{item.name}}</router-link>
                    </li>
                </ul>
            </div>
            <div id="right" class="col-md-8 col-xs-12  wow bounceInRight">
                <router-view></router-view>
            </div>
        </div> -->
         <div id="customer" class="container-fuild">
            <div class=" customer-container">
                  <p class="customer-title text-center">代理商展示</p>
                  <div class="swiper-container customer-swiper hidden-xs">
                  <div class="swiper-wrapper">
                      <div
                      class="swiper-slide customer-block"
                      v-for="(item,index) in customerList"
                      :key="index"
                      >
                      <div class="customer-logo">
                          <img class="center-block" src="https://c.360.cn/assets/images/product/renlianshibieyingjian/feature-0.png" alt="logo">
                      </div>
                      <!-- <div class="customer-yh">
                          <img src="@/assets/img/yinhao.png" alt="引号">
                      </div> -->
                      <div class="customer-content2" style="font-size:18px;font-weight:700;text-align: center;">{{item.title}}</div>
                      <div class="customer-content1" style="margin-top:10px;text-align: center;">
                          <small style="font-size:16px;" v-html="item.content"></small>
                      </div>
                      
                      </div>
                  </div>
                  <!-- 如果需要导航按钮 -->
                  <!-- <div class="swiper-button-prev"></div>
                  <div class="swiper-button-next"></div> -->
                  </div>
                  <div class="row visible-xs customer-block">
                  <div class="col-xs-12" v-for="(item,index) in customerList" :key="index">
                      <div class="customer-logo">
                      <img class="center-block" :src="item.logo" alt="logo">
                      </div>
                      <!-- <div class="customer-yh">
                      <img src="@/assets/img/yinhao.png" alt="引号">
                      </div> -->
                      <div class="customer-content2">
                      <small>{{item.title}}</small>
                      </div>
                      <div class="customer-content1">
                      <small>{{item.content}}</small>
                      </div>
                      
                  </div>
                  </div>
              </div>
        </div>
    </div>
</template>
<script>
import Swiper from "swiper";
import { WOW } from "wowjs";
export default {
    name: 'Software',
    data(){
        return{
            softwareList: [
                {
                    path: '/software/smartTown',
                    name: '智能小镇管理系统'
                },{
                    path: '/software/bigData',
                    name: '大数据管理系统'
                }
            ],
            customerList: [
            {
              logo: require("@/assets/img/logo_hp.png"),
              title:
                "门禁类--人脸识别门禁8寸/5.5寸  ",
              content:
              `<div>86盒式部署、安装便捷</div>
              <div>本地化计算、存储，安全快捷</div>
              <div>触摸屏、全铝合金机身，品质精良</div>
              <div>毫秒级识别、准确易用</div>
              <div>双目识别，安全防伪</div>
              <div>IP65防尘防水，室内室外兼用</div>
              <div>高屏占比，音视频本地播放</div>
              <div>熔断保护，高可用/div>
              <div>测温联动、一体化识别</div>
              <div>支持人脸、IC卡、ID卡、二维码、密码多重验证组合</div>`
            },
            {
              logo: require("@/assets/img/logo_kk.png"),
              title:
                "门禁类--人脸识别门禁8寸/5.5寸  ",
              content:
                `<div>86盒式部署、安装便捷</div>
              <div>本地化计算、存储，安全快捷</div>
              <div>触摸屏、全铝合金机身，品质精良</div>
              <div>毫秒级识别、准确易用</div>
              <div>双目识别，安全防伪</div>
              <div>IP65防尘防水，室内室外兼用</div>
              <div>高屏占比，音视频本地播放</div>
              <div>熔断保护，高可用/div>
              <div>测温联动、一体化识别</div>
              <div>支持人脸、IC卡、ID卡、二维码、密码多重验证组合</div>`
            },
            {
              logo: require("@/assets/img/logo_toyota.png"),
              title:
                "门禁类--人脸识别门禁8寸/5.5寸  ",
              content:
                `<div>86盒式部署、安装便捷</div>
              <div>本地化计算、存储，安全快捷</div>
              <div>触摸屏、全铝合金机身，品质精良</div>
              <div>毫秒级识别、准确易用</div>
              <div>双目识别，安全防伪</div>
              <div>IP65防尘防水，室内室外兼用</div>
              <div>高屏占比，音视频本地播放</div>
              <div>熔断保护，高可用/div>
              <div>测温联动、一体化识别</div>
              <div>支持人脸、IC卡、ID卡、二维码、密码多重验证组合</div>`
            },
            {
              logo: require("@/assets/img/logo_kk.png"),
              title:
                "门禁类--人脸识别门禁8寸/5.5寸  ",
              content:
                `<div>86盒式部署、安装便捷</div>
              <div>本地化计算、存储，安全快捷</div>
              <div>触摸屏、全铝合金机身，品质精良</div>
              <div>毫秒级识别、准确易用</div>
              <div>双目识别，安全防伪</div>
              <div>IP65防尘防水，室内室外兼用</div>
              <div>高屏占比，音视频本地播放</div>
              <div>熔断保护，高可用/div>
              <div>测温联动、一体化识别</div>
              <div>支持人脸、IC卡、ID卡、二维码、密码多重验证组合</div>`
            },
            {
              logo: require("@/assets/img/logo_hp.png"),
              title:
                "门禁类--人脸识别门禁8寸/5.5寸  ",
              content:
                `<div>86盒式部署、安装便捷</div>
              <div>本地化计算、存储，安全快捷</div>
              <div>触摸屏、全铝合金机身，品质精良</div>
              <div>毫秒级识别、准确易用</div>
              <div>双目识别，安全防伪</div>
              <div>IP65防尘防水，室内室外兼用</div>
              <div>高屏占比，音视频本地播放</div>
              <div>熔断保护，高可用/div>
              <div>测温联动、一体化识别</div>
              <div>支持人脸、IC卡、ID卡、二维码、密码多重验证组合</div>`
            },
            {
              logo: require("@/assets/img/logo_toyota.png"),
              title:
                "门禁类--人脸识别门禁8寸/5.5寸  ",
              content:
                `<div>86盒式部署、安装便捷</div>
              <div>本地化计算、存储，安全快捷</div>
              <div>触摸屏、全铝合金机身，品质精良</div>
              <div>毫秒级识别、准确易用</div>
              <div>双目识别，安全防伪</div>
              <div>IP65防尘防水，室内室外兼用</div>
              <div>高屏占比，音视频本地播放</div>
              <div>熔断保护，高可用/div>
              <div>测温联动、一体化识别</div>
              <div>支持人脸、IC卡、ID卡、二维码、密码多重验证组合</div>`
            },
            {
              logo: require("@/assets/img/logo_kk.png"),
              title:
                "门禁类--人脸识别门禁8寸/5.5寸  ",
              content:
                `<div>86盒式部署、安装便捷</div>
              <div>本地化计算、存储，安全快捷</div>
              <div>触摸屏、全铝合金机身，品质精良</div>
              <div>毫秒级识别、准确易用</div>
              <div>双目识别，安全防伪</div>
              <div>IP65防尘防水，室内室外兼用</div>
              <div>高屏占比，音视频本地播放</div>
              <div>熔断保护，高可用/div>
              <div>测温联动、一体化识别</div>
              <div>支持人脸、IC卡、ID卡、二维码、密码多重验证组合</div>`
            },
            {
              logo: require("@/assets/img/logo_hp.png"),
              title:
                "门禁类--人脸识别门禁8寸/5.5寸  ",
              content:
                `<div>86盒式部署、安装便捷</div>
              <div>本地化计算、存储，安全快捷</div>
              <div>触摸屏、全铝合金机身，品质精良</div>
              <div>毫秒级识别、准确易用</div>
              <div>双目识别，安全防伪</div>
              <div>IP65防尘防水，室内室外兼用</div>
              <div>高屏占比，音视频本地播放</div>
              <div>熔断保护，高可用/div>
              <div>测温联动、一体化识别</div>
              <div>支持人脸、IC卡、ID卡、二维码、密码多重验证组合</div>`
            },
            {
              logo: require("@/assets/img/logo_toyota.png"),
              title:
                "门禁类--人脸识别门禁8寸/5.5寸  ",
              content:
                `<div>86盒式部署、安装便捷</div>
              <div>本地化计算、存储，安全快捷</div>
              <div>触摸屏、全铝合金机身，品质精良</div>
              <div>毫秒级识别、准确易用</div>
              <div>双目识别，安全防伪</div>
              <div>IP65防尘防水，室内室外兼用</div>
              <div>高屏占比，音视频本地播放</div>
              <div>熔断保护，高可用/div>
              <div>测温联动、一体化识别</div>
              <div>支持人脸、IC卡、ID卡、二维码、密码多重验证组合</div>`
            },
            {
              logo: require("@/assets/img/logo_hp.png"),
              title:
                "门禁类--人脸识别门禁8寸/5.5寸  ",
              content:
                `<div>86盒式部署、安装便捷</div>
              <div>本地化计算、存储，安全快捷</div>
              <div>触摸屏、全铝合金机身，品质精良</div>
              <div>毫秒级识别、准确易用</div>
              <div>双目识别，安全防伪</div>
              <div>IP65防尘防水，室内室外兼用</div>
              <div>高屏占比，音视频本地播放</div>
              <div>熔断保护，高可用/div>
              <div>测温联动、一体化识别</div>
              <div>支持人脸、IC卡、ID卡、二维码、密码多重验证组合</div>`
            },
            {
              logo: require("@/assets/img/logo_kk.png"),
              title:
                "门禁类--人脸识别门禁8寸/5.5寸  ",
              content:
                `<div>86盒式部署、安装便捷</div>
              <div>本地化计算、存储，安全快捷</div>
              <div>触摸屏、全铝合金机身，品质精良</div>
              <div>毫秒级识别、准确易用</div>
              <div>双目识别，安全防伪</div>
              <div>IP65防尘防水，室内室外兼用</div>
              <div>高屏占比，音视频本地播放</div>
              <div>熔断保护，高可用/div>
              <div>测温联动、一体化识别</div>
              <div>支持人脸、IC卡、ID卡、二维码、密码多重验证组合</div>`
            },
            {
              logo: require("@/assets/img/logo_hp.png"),
              title:
                "门禁类--人脸识别门禁8寸/5.5寸  ",
              content:
                `<div>86盒式部署、安装便捷</div>
              <div>本地化计算、存储，安全快捷</div>
              <div>触摸屏、全铝合金机身，品质精良</div>
              <div>毫秒级识别、准确易用</div>
              <div>双目识别，安全防伪</div>
              <div>IP65防尘防水，室内室外兼用</div>
              <div>高屏占比，音视频本地播放</div>
              <div>熔断保护，高可用/div>
              <div>测温联动、一体化识别</div>
              <div>支持人脸、IC卡、ID卡、二维码、密码多重验证组合</div>`
            }
          ],
        }
    },
    mounted() {
        /* customer-swiper */
    new Swiper(".customer-swiper", {
      loop: true, // 循环模式选项
      slidesPerView: 3,
      //自动播放
      autoplay: {
        delay: 300000,
        stopOnLastSlide: false,
        disableOnInteraction: false
      },
      // 如果需要前进后退按钮
      navigation: {
        nextEl: ".swiper-button-next",
        prevEl: ".swiper-button-prev"
      },
      observer: true, //修改swiper自己或子元素时，自动初始化swiper
      observeParents: true //修改swiper的父元素时，自动初始化swiper
    });
        var wow = new WOW();
        wow.init();
    },
}
</script>
<style scoped>
#left{
    margin: 50px 0;
}
.left-container{
    width: 60%;
    margin: 0 auto;
    border: 1px solid #474747;
    border-radius: 5px;
}
.left-container>p{
    text-align: center;
    line-height: 45px;
    padding: 0;
    margin: 0;
    background: #474747;
    color: #fff;
    font-size: 18px;
    font-weight: bold;
}
.left-container>li {
  text-align: center;
  height: 38px;
  line-height: 38px;
  margin: 0;
  border-top: 1px solid #474747;
}
.left-container>li>a{
    text-decoration: none;
}
.left-container>li:hover{
    background: #928989;
}
#right{
    padding: 50px 0;
}
#customer {
  padding: 50px 0;
  box-sizing: border-box;
  /* background: #efefef; */
  transition: all ease 0.6s;
}
#customer .customer-title {
  font-size: 30px;
  color: rgb(102, 102, 102);
  margin: 0 0 30px;
}
#customer .customer-block {
  background: #fff;
  padding: 30px;
}
#customer .customer-logo img {
  width: 300px;
  height: 200px;
  /* border: 1px solid #ccc; */
}
#customer .customer-yh img {
  width: 34px;
  height: 34px;
}
#customer .customer-content1 {
  padding-bottom: 20px;
  /* border-bottom: 1px solid #0ce9f1; */
}
#customer .customer-content2 {
  padding-top: 20px;
}
@media screen and (max-width: 768px){
    #right{
        padding: 15px;
    }
}
</style>

