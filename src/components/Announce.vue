<template>
 <div class="announce">
  <img src="@/assets/notice.png" alt="">
  <!-- 扣叮头条轮播 -->
  <Carousel  v-model="value1" loop autoplay dots="none" radius-dot arrow="never">
      <CarouselItem class="carousel" v-for="(item,index) in topList" :key="index">
          <div class="demo-carousel">
            {{item}} 
          </div>
          <img v-if="index===2" class="notice-tag" src="@/assets/new.png" alt="">
          <img v-else class="notice-tag" src="@/assets/hot.png" alt="">
          
      </CarouselItem>
  </Carousel>
 </div>
</template>
<script>
  export default {
      data () {
          return {
              value1: 0,
              topList: ['追梦导师，助梦成真', '追梦营移动站上线啦！！！', '追梦四年，以科技助力乡村教育普惠培养科技创新人才']
          }
      }
  }
</script>
<style lang="less" scoped>
.announce{
  width: 1200px;
  height: 70px;
  line-height: 70px;
  margin-left: 50px;
  background-color: #fff;
  border-radius: 0 0 12px 12px;
  padding: 0 28px;
  img{
    width: 138px;
    height: 30px;
    float: left;
    margin-top: 20px;
  }
  .notice-tag{
    width: 36px;
    height: 16px;
    line-height: 16px;
    border-radius: 8px 8px 8px 0;
    text-align: center;
    font-size: 12px;
    color: #fff;
    .hot{
      background-color: #EB676A;
    }
    
  }
  .carousel{
    display: flex;
    
    .notice-tag{
      width: 40px;
      height: 20px;
    }
  }
}

</style>