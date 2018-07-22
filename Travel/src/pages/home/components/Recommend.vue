<template>
  <div>
     <div class="title">热销推荐</div>
     <ul>
       <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
        <img class="item-img" :src="item.imgUrl" alt="item.title">
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
        id: '001',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/201408/14/dba7220ac844600c07a1af703f640935.jpg_200x200_a84b7d79.jpg',
        title: '杭州乐园',
        desc: '杭州乐园杭州乐园杭州乐园杭州乐园杭州乐园杭州乐园杭州乐园'
      }, {
        id: '002',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/201408/14/dba7220ac844600c07a1af703f640935.jpg_200x200_a84b7d79.jpg',
        title: '杭州乐园',
        desc: '杭州乐园杭州乐园杭州乐园杭州乐园杭州乐园杭州乐园杭州乐园'
      }, {
        id: '003',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/201408/14/dba7220ac844600c07a1af703f640935.jpg_200x200_a84b7d79.jpg',
        title: '杭州乐园',
        desc: '杭州乐园杭州乐园杭州乐园杭州乐园杭州乐园杭州乐园杭州乐园'
      }, {
        id: '004',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/201408/14/dba7220ac844600c07a1af703f640935.jpg_200x200_a84b7d79.jpg',
        title: '杭州乐园',
        desc: '杭州乐园杭州乐园杭州乐园杭州乐园杭州乐园杭州乐园杭州乐园'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
@import '~styles/mixins.styl'
.title
  margin-top .2rem
  line-height .8rem
  background #eeeeee
  text-indent .2rem
.item
  display flex
  height 1.9rem
  overflow hidden
  .item-img
    width 1.7rem
    height 1.7rem
    padding .1rem
  .item-info
    min-width 0
    flex 1
    .item-title
      line-height .54rem
      font-size .32rem
      ellipsis()
    .item-desc
      line-height .4rem
      color #ccc
      ellipsis()
    .item-button
      line-height .44rem
      background #ff9300
      margin-top .16rem
      padding 0 .2rem
      border-radius .06rem
      color #fff
</style>
