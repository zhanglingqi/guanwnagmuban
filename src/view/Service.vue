<template>
    <div id="Service">
        <div class="container text-center">
            <h3>我们的服务</h3>
            <p style="color:#b2b2b2">The Best Service You Never See</p>
        </div>
        <div class="container">
            <!-- <div class="Service-container row">
                <div class="Service-item col-xs-12 col-sm-6 col-md-3 wow slideInUp" 
                v-for="(item,index) in serviceList" :key="index" @click="ServiceClick(item.id)">
                    <div class="Service-item-wrapper">
                        <div class="Service-item-top">
                            <h4>{{item.title}}</h4>
                            <i></i>
                            <p>{{item.eng_title}}</p>
                        </div>
                        <div class="Service-item-img">
                            <img :src="item.img" alt="服务">
                        </div>
                        <div class="Service-item-border"></div>
                    </div>
                </div>
            </div> -->
                  <div class=" customer-container">
                  <!-- <p class="customer-title text-center">代理商展示</p> -->
                  <div class="swiper-container customer-swiper hidden-xs">
                  <div class="swiper-wrapper">
                      <div
                      class="swiper-slide customer-block"
                      v-for="(item,index) in customerList"
                      :key="index"
                      >
                      <div class="customer-logo">
                          <img class="center-block" src="https://c.360.cn/assets/images/solution/shijueanquan/scene-0.png" alt="logo">
                      </div>
                      <!-- <div class="customer-yh">
                          <img src="@/assets/img/yinhao.png" alt="引号">
                      </div> -->
                      <div class="customer-content2" style="font-size:18px;font-weight:700;text-align: left;">{{item.title}}</div>
                      <div class="line"></div>
                      <div style="display:inline-block;margin-top:10px">业务需求</div>
                      <div class="customer-content1" style="margin-top:10px;text-align: left;">
                          <small style="font-size:16px;" v-html="item.content"></small>
                      </div>
                      <div class="line"></div>
                      <div style="display:inline-block;margin-top:10px">解决方案</div>
                      <div class="customer-content1" style="margin-top:10px;text-align: left;">
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
import { WOW } from 'wowjs';
export default {
    name: 'Service',
    data(){
        return{
            serviceList: [
                {
                    id: 'section-1',
                    title: '软件定制开发',
                    eng_title: 'Customize App',
                    img: require('@/assets/img/service1.jpg')
                },{
                    id: 'section-2',
                    title: 'IT外包服务',
                    eng_title: 'Outsourcing',
                    img: require('@/assets/img/service2.jpg')
                },{
                    id: 'section-3',
                    title: '网上商城建设',
                    eng_title: 'eCommerce Site',
                    img: require('@/assets/img/service3.jpg')
                },{
                    id: 'section-4',
                    title: 'iOS应用定制开发',
                    eng_title: 'iOS App Dev',
                    img: require('@/assets/img/service4.jpg')
                }
            ],
            customerList: [
            {
              logo: require("@/assets/img/logo_hp.png"),
              title: "智慧园区",
              content:
              `将人工智能融入到园区的日常管理中，实现园区区域管控、人员身份验证、提供考勤、门禁、访客的一体化管理，为园区提供人脸识别大数据支撑。提升产业园区的内部管理水平和服务水平。主要面临的痛点有：信息化程度不高、人员众多、管理复杂、管控成本高；信息泄露，园区安全问题突出；传统刷卡方式，数据真伪难辨；难以满足政府及公安等行业管理部门的管理要求`
            },
            {
              logo: require("@/assets/img/logo_kk.png"),
              title:
                "智慧校园",
              content:
                `将人脸识别技术与校园的管理系统有机的结合，应用在高校的公共安全、考勤管理、访客管理、考试管理、图书馆管理、宿舍管理、实验室管理、校园社区管理等教学与生活场景之中， 打造更加安全、便捷的新时代校园环境`
            },
            {
              logo: require("@/assets/img/logo_hp.png"),
              title:
                "智慧园区",
              content:
              `将人工智能融入到园区的日常管理中，实现园区区域管控、人员身份验证、提供考勤、门禁、访客的一体化管理，为园区提供人脸识别大数据支撑。提升产业园区的内部管理水平和服务水平。主要面临的痛点有：信息化程度不高、人员众多、管理复杂、管控成本高；信息泄露，园区安全问题突出；传统刷卡方式，数据真伪难辨；难以满足政府及公安等行业管理部门的管理要求`
            },
            {
              logo: require("@/assets/img/logo_kk.png"),
              title:
                "智慧校园",
              content:
                `将人脸识别技术与校园的管理系统有机的结合，应用在高校的公共安全、考勤管理、访客管理、考试管理、图书馆管理、宿舍管理、实验室管理、校园社区管理等教学与生活场景之中， 打造更加安全、便捷的新时代校园环境`
            },
          ],
        }
    },
    mounted(){
        new Swiper(".customer-swiper", {
        loop: true, // 循环模式选项
        slidesPerView: 2,
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
    methods:{
        ServiceClick(id){
            this.$router.push({
                name: 'servicedetail',
                params: {
                    id: id
                }
            })
        }
    }
}
</script>
<style scoped>
.container img {
    width: 100%;
    height: 100%;
}
.Service-container{
    padding: 30px 50px;
}
.Service-item{
    margin-bottom: 50px;
}
.Service-item-wrapper{
    cursor: pointer;
    background: rgba(244,244,244,1);
    overflow: hidden;
    position: relative;
}
.Service-item-top{
    width: 100%;
    height: 120px;
    padding: 30px;
    text-align: center;
}
.Service-item-top>i{
    display: inline-block;
    width: 25px;
    height: 2px;
    background: #28f;
}
.Service-item-top>p{
    color: #b2b2b2;
    opacity: 0;
    transform: translateY(10px);
    transition: all .5s ease;
}
.Service-item-img{
    width: 100%;
    overflow: hidden;
}
.Service-item-img img{
    width: 100%;
    transition: all 0.5s ease;
}
.Service-item-border{
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    margin: auto;
    z-index: 9999999;
    width: 100%;
    height: 100%;
    transition: all 0.5s ease;
    border: 1px solid #000;
    opacity: 0;
}
.Service-item-wrapper:hover .Service-item-top > i{
    opacity: 0;
}
.Service-item-wrapper:hover .Service-item-top > p{
    opacity: 1;
    transform: translateY(-10px);
}
.Service-item-wrapper:hover .Service-item-img > img{
    transform: scale(1.1,1.1);
}
.Service-item-wrapper:hover > .Service-item-border{
    opacity: 1;
    width: 90%;
    height: 90%;
}

.container {
  /* padding: 50px 0; */
  box-sizing: border-box;
  /* background: #efefef; */
  transition: all ease 0.6s;
}
.container .customer-title {
  font-size: 30px;
  color: rgb(102, 102, 102);
  margin: 0 0 30px;
}
.container .customer-block {
  background: #fff;
  padding: 30px;
}
.container .customer-logo img {
  width: 100%;
    height: 220px;
    /* border: 1px solid #ccc; */
}
.container .customer-yh img {
  width: 34px;
  height: 34px;
}
.container .customer-content1 {
  padding-bottom: 20px;
  /* border-bottom: 1px solid #0ce9f1; */
}
.container .customer-content2 {
  padding-top: 20px;
}
.line {
    display:inline-block;
    width: 5px;
    height: 14px;
    background-color: #2cff00;
}
</style>

