<style lang="less" scoped>
  @import "../assets/css/swiper_table.less";
  .top_header{
    height: 60px;
    line-height: 60px;
    width: 100%;
    font-size: 16px;
    color: black;
    opacity: 0.8;
  }
</style>
<template>
  <div>
  <div class="top_header">
      移动端滑动表格组件
  </div>
  <div class="topNav_all">
    <div class="topNav_left">
      <div class="topNav_title">
        <span class="fix-active">测试1</span>
      </div>
      <div class="topNav_title">
        <span class="fix-active">测试2</span>
      </div>
      <div class="topNav_title">
        <span class="fix-active">测试3</span>
      </div>
      <div class="topNav_title">
        <span class="fix-active">测试4</span>
      </div>
      <div class="topNav_title">
        <span class="fix-active">测试5</span>
      </div>
    </div>
    <ul id="topNav" class="swiper-container">
      <li class="swiper-wrapper">
        <div class="swiper-slide"><span>S1100</span></div>
        <div class="swiper-slide"><span>S1101</span></div>
        <div class="swiper-slide"><span>S1102</span></div>
        <div class="swiper-slide"><span>S1103</span></div>
        <div class="swiper-slide"><span>S1104</span></div>
      </li>
      <li class="swiper-wrapper">
        <div class="swiper-slide1"><span>11-02(四)</span></div>
        <div class="swiper-slide1"><span>11-02(四)</span></div>
        <div class="swiper-slide1"><span>11-02(四)</span></div>
        <div class="swiper-slide1"><span>11-02(四)</span></div>
        <div class="swiper-slide1"><span>11-02(四)</span></div>
      </li>
      <li class="swiper-wrapper">
        <div class="swiper-slide1"><span>29</span></div>
        <div class="swiper-slide1"><span>29</span></div>
        <div class="swiper-slide1"><span>29</span></div>
        <div class="swiper-slide1"><span>29</span></div>
        <div class="swiper-slide1"><span>29</span></div>
      </li>
      <li class="swiper-wrapper">
        <div class="swiper-slide1"><span>29</span></div>
        <div class="swiper-slide1"><span>29</span></div>
        <div class="swiper-slide1"><span>29</span></div>
        <div class="swiper-slide1"><span>29</span></div>
        <div class="swiper-slide1"><span>29</span></div>

      </li>
      <li class="swiper-wrapper">
        <div class="swiper-slide1"><span>29</span></div>
        <div class="swiper-slide1"><span>29</span></div>
        <div class="swiper-slide1"><span>29</span></div>
        <div class="swiper-slide1"><span>29</span></div>
        <div class="swiper-slide1"><span>29</span></div>
      </li>

    </ul>
  </div>
  </div>
</template>
<script>
  import Swiper from 'swiper';
  import 'swiper/dist/css/swiper.min.css';
  export  default{
      data(){
          return{

          }
      },
    created: function () {
      this.$nextTick(() => {
        this.initTable();
      });
    },
    methods:{
      initTable(){
        if (this.swiper_ins) {
          this.swiper_ins.destroy();
        }
        this.swiper_ins = new Swiper('#topNav', {
          freeMode: true,
          slidesPerView: 'auto',
          resistanceRatio: 0,
        });
      },
    }
  }
</script>
