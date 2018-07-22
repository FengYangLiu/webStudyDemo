<template>
  <div>
     <div class="title">周末去哪儿</div>
     <ul>
       <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
        <div class="item-img-wrapper">
          <img class="item-img" :src="item.imgUrl" alt="item.title">
        </div>
         <div class="item-info">
           <p class="item-title">{{item.title}}</p>
           <p class="item-desc">{{item.desc}}</p>
         </div>
       </li>
     </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  data () {
    return {
      recommendList: [{
        id: '001',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/9f/7d45cc38259e0.jpg_r_640x214_156f4299.jpg',
        title: '杭州乐园',
        desc: '杭州乐园杭州乐园杭州乐园杭州乐园杭州乐园杭州乐园杭州乐园'
      }, {
        id: '002',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/9f/7d45cc38259e0.jpg_r_640x214_156f4299.jpg',
        title: '杭州乐园',
        desc: '杭州乐园杭州乐园杭州乐园杭州乐园杭州乐园杭州乐园杭州乐园'
      }, {
        id: '003',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/9f/7d45cc38259e0.jpg_r_640x214_156f4299.jpg',
        title: '杭州乐园',
        desc: '杭州乐园杭州乐园杭州乐园杭州乐园杭州乐园杭州乐园杭州乐园'
      }, {
        id: '004',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/9f/7d45cc38259e0.jpg_r_640x214_156f4299.jpg',
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
.item-img-wrapper
  overflow hidden
  height 0
  padding-bottom 33.9%
  .item-img
    width 100%
.item-info
  padidng .1rem
  .item-title
    line-height .54rem
    font-size .32rem
    ellipsis()
  .item-desc
    line-height .4rem
    color #ccc
    ellipsis()
</style>
