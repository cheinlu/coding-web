<template>
  <div class="banner-container">
    <!-- 图片轮播图 -->
    <Carousel v-model="value" loop autoplay dots="none" radius-dot arrow="never">
      <CarouselItem>
        <div class="demo-carousel">
          <img src="@/assets/slide-img-1.jpg" alt="" />
        </div>
      </CarouselItem>
      <CarouselItem>
        <div class="demo-carousel">
          <img src="@/assets/slide-img-2.jpg" alt="" />
        </div>
      </CarouselItem>
      <CarouselItem>
        <div class="demo-carousel">
          <img src="@/assets/slide-img-3.jpg" alt="" />
        </div>
      </CarouselItem>
      <CarouselItem>
        <div class="demo-carousel">
          <img src="@/assets/slide-img-4.jpg" alt="" />
        </div>
      </CarouselItem>
      <CarouselItem>
        <div class="demo-carousel">
          <img src="@/assets/slide-img-5.jpg" alt="" />
        </div>
      </CarouselItem>
    </Carousel>
    <!-- 文字导航 -->
    <div class="slide-nav">
      <div @click="dian(0)" class="slide-nav-pre">
        <a href="#">
          <Icon type="ios-arrow-back" size="30" />
        </a>
      </div>
      <div class="slide-nav-item" v-for="(item, index) in list" :key="index" @click="value = index">
        <a v-if="value === index" class="active" href="#">{{ item }}</a>
        <a v-else href="#">{{ item }}</a>
      </div>
      <div @click="dian(1)">
        <a href="#" class="slide-nav-btn">
          <Icon type="ios-arrow-forward" size="30" />
        </a>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      value: 0,
      list: ['2023NOC扣叮创意编程', '从边陲小镇到编程小镇', '编程与人工智能活动', '腾讯游戏年度故事片', '代码世界里的乡村教师']
    }
  },
  methods: {
    dian(type) {
      const index = this.value
      if (type) {
        this.value = index === 4 ? 0 : index + 1
      } else {
        this.value = index === 0 ? 4 : index - 1
      }
    }
  }
}
</script>
<style lang="less" scoped>
.banner-container {
  max-width: 1920px;
  position: relative;
  box-sizing: border-box;
  overflow: hidden;
  img {
    width: 100%;
    height: 300px;
  }
  .slide-nav {
    margin-left: 50px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 1200px;
    height: 50px;
    background-color: rgba(255, 255, 255, 0.8);
    border-radius: 12px 12px 0 0;
    position: absolute;
    bottom: 0;
    z-index: 9;
    .slide-nav-item {
      flex: 1;
      width: 220px;
      height: 50px;
      line-height: 50px;
      text-align: center;
      border-right: 1px solid rgba(255, 255, 255, 0.6);
      &::after {
        content: '';
        position: absolute;
        left: 0;
        bottom: 0;
        height: 3px;
        width: 100%;
        background: linear-gradient(rgba(255, 255, 255, 0), rgba(0, 0, 0, 0.1));
      }
    }
    .active {
      color: #009cff;
      position: relative;
      &::after {
        content: ' ';
        position: absolute;
        bottom: -17px;
        left: 50%;
        transform: translateX(-50%);
        height: 3px;
        width: 222px;
        background-color: #009cff;
      }
    }
    .slide-nav-pre {
      // width: 50px;
      height: 50px;
      line-height: 50px;
      border-right: 1px solid rgba(255, 255, 255, 0.6);
    }
    a {
      color: #4a596f;
      &:hover {
        color: #009cff;
      }
    }
  }
}
</style>
