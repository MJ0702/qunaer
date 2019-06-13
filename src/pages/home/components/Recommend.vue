<template>
  <div>
    <div class="title">热销推荐</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
        <img class="item-img" :src="item.imgUrl" alt="">
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-button">查看详情</button>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1906/eb/eb39cce9ccab5cada3.img.jpg_200x200_e409a517.jpg',
        title: '锦绣中华民俗村',
        desc: '一步迈进历史，一天游遍中华'
      },
      {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1905/e6/e683c8cf5e97ce03a3.img.jpg_200x200_4769276c.jpg',
        title: '世界之窗',
        desc: '国际啤酒节清凉一夏，夜场49.9元'
      },
      {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/201307/18/f25ac054eec3804dc8d65eac.jpg_200x200_a008b6ca.jpg',
        title: '海洋奇梦馆',
        desc: '海洋奇梦馆，带你寻找童年的海洋梦'
      },
      {
        id: '0004',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1808/48/48ae3e0f9a3f195ca3.img.jpg_200x200_f2195465.jpg',
        title: 'Skyland未来科技馆',
        desc: '深圳新的亲子游乐打卡圣地'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
 .title
    margin-top:.2rem
    line-height:.8rem
    background:#eee
    text-indent:.2rem
  .item
    overflow:hidden
    display:flex
    height:1.9rem
    .item-img
      width:1.7rem
      height:1.7rem
      padding:.1rem
    .item-info
      flex:1
      padding:.1rem
      min-width:0
      .item-title
        line-height:.54rem
        font-size:.32rem
        ellipsis()
      .item-desc
        line-height:.4rem
        color:#ccc
        ellipsis()
      .item-button
        line-height:.44rem
        margin-top:.16rem
        background:#ff9300
        padding:0 .2rem
        border-radius:.06rem
        color:#fff
</style>
