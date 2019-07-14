<template>
  <div class="wrap">
    <div class="top">
      <Carousel autoplay v-model="value1" loop >
        <CarouselItem v-for="(item,index) in imgList" :key="index">
          <!--<div class="demo-carousel">-->
          <img class="scan-img" :src="item.image"  :alt="item.desc">
          <!--</div>-->
        </CarouselItem>
      </Carousel>
    </div>
    <!--<div class="react">-->
      <!--<div class="floor-wrap">-->
        <!--<div class="floor-title">美食</div>-->
        <!--<Row :gutter="16">-->
          <!--<Col span="6">-->
            <!--<div class="floor-item">-->
              <!--<img class="floor-img" src="@/../static/images/food1.jpg">-->
              <!--<span class="floor-text">帝王蟹</span>-->
            <!--</div>-->
          <!--</Col>-->
          <!--<Col span="6">-->
            <!--<div class="floor-item">-->
              <!--<img class="floor-img" src="@/../static/images/food1.jpg">-->
              <!--<span class="floor-text">帝王蟹</span>-->
            <!--</div>-->
          <!--</Col>-->
          <!--<Col span="6">-->
          <!--<div class="floor-item">-->
            <!--<img class="floor-img" src="@/../static/images/food1.jpg">-->
            <!--<span class="floor-text">帝王蟹</span>-->
          <!--</div>-->
        <!--</Col>-->
          <!--<Col span="6">-->
          <!--<div class="floor-item">-->
            <!--<img class="floor-img" src="@/../static/images/food1.jpg">-->
            <!--<span class="floor-text">帝王蟹</span>-->
          <!--</div>-->
        <!--</Col>-->
        <!--</Row>-->
      <!--</div>-->
    <!--</div>-->
  </div>
</template>

<script>
export default {
  name: 'home',
  data () {
    return {
      value1: 0,
      imgList: [
        {
          desc: '小镇',
          image: '../../../static/images/1.jpg'
        },
        {
          desc: '小镇',
          image: '../../../static/images/2.jpg'
        },
        {
          desc: '小镇',
          image: '../../../static/images/3.jpg'
        }
      ]

    }
  }
}
</script>

<style scoped>
  .wrap{
    margin: 0;
    padding: 0;
    background: #efefef;
  }
  /*.top{*/
    /*width: 100%;*/
    /*!*height: 600px;*!*/
  /*}*/
  .top{
    width: 100%;
    background: #fff;
  }
  .scan-img{
    width: 100%;
    height: 600px;
  }
  .react{
    width: 100%;
    background: #fff;
    margin: 20px 0;

  }
  .floor-item{
    width: 420px;
    height: 450px;
    margin-right: 20px;
  }
  .floor-img{
    width: 100%;
    height: 90%;
  }
</style>
