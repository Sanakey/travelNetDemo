<template>
  <div>
    <div class="title">热销推荐</div>
    <ul >
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
        <div class="item-img-wrapper">
          <img class="item-img" :src="item.imgUrl" />
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
      recommendList: [
        {
          id: '001',
          imgUrl: 'http://img1.qunarzz.com/sight/source/1606/88/56f7f4bd0493fe.jpg_r_640x214_f8c0994a.jpg',
          title: '广州长隆度假区',
          desc: '来广州来长隆，就对了，就够了~'
        },
        {
          id: '002',
          imgUrl: 'http://img1.qunarzz.com/sight/source/1505/96/c5401993cd3b48.jpg_r_640x214_18948dd3.jpg',
          title: '广州长隆度假区',
          desc: '来广州来长隆，就对了，就够了~'
        },
        {
          id: '003',
          imgUrl: 'http://img1.qunarzz.com/sight/source/1505/50/07fa9343791682.jpg_r_640x214_c8c3d798.jpg',
          title: '广州长隆度假区',
          desc: '来广州来长隆，就对了，就够了~'
        }
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .title
    line-height: .8rem
    background: #eee
    text-indent: .2rem
  .item-img-wrapper
    overflow: hidden
    height: 0
    padding-bottom: 37.09%
    .item-img
      width: 100%
  .item-info
    padding: .1rem
    .item-title
      line-height: .54rem
      font-size: .32rem
      ellipsis()
    .item-desc
      line-height: .4rem
      color: #ccc
      ellipsis()
</style>
