<template>
  <div class="home">
    <!--首页头部-->
    <HeaderTop :title="address.name">
       <span class="header_search" slot="left">
         <i class="iconfont icon-sousuo"></i>
       </span>
      <span class="header_login" slot="right">
        <span class="header_login_text">登录|注册</span>
    </span>
    </HeaderTop>
    <!--首页导航-->
    <nav class="home_nav">
      <van-swipe class="my-swipe"  indicator-color="#02a774">
        <van-swipe-item class="my-swipe-item">
           <span class="link_to_food">
              <div class="food_container">
                <img src="./images/nav/1.jpg">
              </div>
              <span>甜品饮品</span>
            </span>
          <span class="link_to_food">
              <div class="food_container">
                <img src="./images/nav/2.jpg">
              </div>
              <span>商超便利</span>
            </span>
          <span class="link_to_food">
              <div class="food_container">
                <img src="./images/nav/3.jpg">
              </div>
              <span>美食</span>
            </span>
          <span class="link_to_food">
              <div class="food_container">
                <img src="./images/nav/4.jpg">
              </div>
              <span>简餐</span>
            </span>
          <span class="link_to_food">
              <div class="food_container">
                <img src="./images/nav/5.jpg">
              </div>
              <span>新店特惠</span>
            </span>
          <span class="link_to_food">
              <div class="food_container">
                <img src="./images/nav/6.jpg">
              </div>
              <span>准时达</span>
            </span>
          <span class="link_to_food">
              <div class="food_container">
                <img src="./images/nav/7.jpg">
              </div>
              <span>预订早餐</span>
            </span>
          <span class="link_to_food">
              <div class="food_container">
                <img src="./images/nav/8.jpg">
              </div>
              <span>土豪推荐</span>
            </span>
        </van-swipe-item>
        <van-swipe-item class="my-swipe-item">
            <span class="link_to_food">
              <div class="food_container">
                <img src="./images/nav/9.jpg">
              </div>
              <span>甜品饮品</span>
            </span>
          <span class="link_to_food">
              <div class="food_container">
                <img src="./images/nav/10.jpg">
              </div>
              <span>商超便利</span>
            </span>
          <span class="link_to_food">
              <div class="food_container">
                <img src="./images/nav/11.jpg">
              </div>
              <span>美食</span>
            </span>
          <span class="link_to_food">
              <div class="food_container">
                <img src="./images/nav/12.jpg">
              </div>
              <span>简餐</span>
            </span>
          <span  class="link_to_food">
              <div class="food_container">
                <img src="./images/nav/13.jpg">
              </div>
              <span>新店特惠</span>
            </span>
          <span class="link_to_food">
              <div class="food_container">
                <img src="./images/nav/14.jpg">
              </div>
              <span>准时达</span>
            </span>
          <span class="link_to_food">
              <div class="food_container">
                <img src="./images/nav/1.jpg">
              </div>
              <span>预订早餐</span>
            </span>
          <span class="link_to_food">
              <div class="food_container">
                <img src="./images/nav/2.jpg">
              </div>
              <span>土豪推荐</span>
            </span>
        </van-swipe-item>
      </van-swipe>
    </nav>
    <!--首页附近商家-->
    <div class="home_shop_list">
      <div class="shop_header">
        <i class="iconfont icon-xuanxiang"></i>
        <span class="shop_header_title">附近商家</span>
      </div>
      <ShopList/>
    </div>
  </div>
</template>

<script>
import HeaderTop from '@/components/HeaderTop/HeaderTop'
import ShopList from '@/components/ShopList/ShopList'
import { mapState } from 'vuex'
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: 'Home',
  computed: {
    ...mapState(['address'])
  },
  components: { ShopList, HeaderTop }
}
</script>

<style scoped lang="less">

.home {
  width: 100%;
}

.home_nav {
  position: relative;
  margin-top: 45px;
  height: 200px;
  background: #fff;
}
.home_nav::before {
  content: '';
  position: absolute;
  z-index: 200;
  left: 0;
  bottom: 0;
  width: 100%;
  height: 1px;
  background-color: #e4e4e4;
  transform: scaleY(0.5);
}

.home_nav .my-swipe{
  width: 100%;
  height: 100%;
}
.home_nav  .my-swipe .my-swipe-item{
  display: flex;
  justify-content: center;
  //align-items: flex-start;
  flex-wrap: wrap;
}
.link_to_food {
  width: 25%;
}
.food_container {
  display: block;
  width: 100%;
  text-align: center;
  padding-bottom: 10px;
  font-size: 0;
}
.food_container img {
  display: inline-block;
  width: 50px;
  height: 50px;
}
.link_to_food span {
  display: block;
  width: 100%;
  text-align: center;
  font-size: 13px;
  color: #666;
}
.home_shop_list{
  position: relative;
  margin-top: 10px;
  background: #fff;
}
.home_shop_list::before {
  content: '';
  position: absolute;
  z-index: 200;
  left: 0;
  top: 0;
  width: 100%;
  height: 1px;
  background-color: #e4e4e4;
}
.shop_header {
  padding: 10px 10px 0;
}
.shop_header_title {
  color: #999;
  font-size: 14px;
  line-height: 20px;
}

/*.shop_rating_order .shop_rating_order_right {*/
/*  float: right;*/
/*  font-size: 0;*/
/*}*/
</style>
