<template>
  <section class="order">
    <HeaderTop title="订单列表" />
    <section class="order_no_login">
      <img src="../Home/images/order/person.png">
      <h3>登录后查看外卖订单</h3>
      <button>立即登陆</button>
    </section>
  </section>
</template>

<script>
import HeaderTop from '@/components/HeaderTop/HeaderTop'
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: 'Order',
  components: { HeaderTop }
}
</script>

<style scoped>

section.order {
  width: 100%;
}
section.order .order_no_login {
  padding-top: 140px;
  width: 60%;
  margin: 0 auto;
  text-align: center;
}
.order_no_login >img {
  display: block;
  width: 100%;
  height: 30%;
}
.order_no_login >h3 {
  padding: 10px 0;
  font-size: 17px;
  color: #6a6a6a;
}
.order_no_login >button {
  display: inline-block;
  background: #02a774;
  font-size: 14px;
  color: #fff;
  border: 0;
  outline: none;
  border-radius: 5px;
  padding: 10px 20px;
}
</style>
