<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
    <!-- slides -->
      <swiper-slide v-for="item of swiperList" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl">
      </swiper-slide>
      <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      },
      swiperList: [{
        id: '0001',
        imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20195/d1dabef55b4e17db42b4d74cc0ea23af.jpg_750x200_5a5c28d4.jpg'
      },
      {
        id: '0002',
        imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/b23a39921e8b78f38b61412d691d93ea.jpg_750x200_942ed7bd.jpg'
      },
      {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1806/ec/865b3fa81806f802.jpg_750x200_7ae07dcd.jpg'
      },
      {
        id: '0004',
        imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/87a224d0349d94a11e97f31aa1aba4f5.jpg_750x200_1f78af87.jpg'
      },
      {
        id: '0005',
        imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20195/2d971885c2a646dd20a55acce76efd35.jpg_750x200_c66112a8.jpg'
      }
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
  .wrapper >>> .swiper-pagination-bullet-active
    background:#FFF
  .wrapper
    overflow:hidden
    width:100%
    height:0
    padding-bottom:26.67%
    background:#eee
    .swiper-img
      width:100%
</style>
