<template>
    <div>
        <div class="recommend-title">热销推荐</div>
        <ul>
            <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
                <img class="item-img" :src="item.imgUrl" />
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
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1607/7c/7cda8b6782dabd80b4.img.jpg_200x200_2039e660.jpg',
        title: '上海迪士尼乐园',
        desc: '上海市浦东新区川沙新镇上海迪士尼度假区内'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1609/80/8092254b7f5f016ea3.water.jpg_200x200_cd798d39.jpg',
        title: '上海欢乐谷',
        desc: '上海市松江区佘山镇林湖路888号'
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/tuan/team2/1507/2c/83e0e0e7ae082a.jpg_200x200_6d7378b2.jpg',
        title: '东方明珠',
        desc: '上海市浦东新区川沙新镇上海迪士尼度假区内'
      }, {
        id: '0004',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1603/17/170481fb9caf500790.water.jpg_200x200_a32b9a92.jpg',
        title: '上海迪野生动物园',
        desc: '上海市浦东新区川沙新镇上海迪士尼度假区内'
      }, {
        id: '0005',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1411/4f/146031f0bc5d7e0dd960d3f5bf0c9eca.water.jpg_200x200_f22705c9.jpg',
        title: '上海科技馆',
        desc: '上海市浦东新区川沙新镇上海迪士尼度假区内'
      }, {
        id: '0006',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1506/30/7a528fae12c17e6e29d5d13a9d9813ee.water.jpg_200x200_e7f0d0ad.jpg',
        title: '上海玛雅海滩水公园',
        desc: '上海市浦东新区川沙新镇上海迪士尼度假区内'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
    @import '~styles/mixins.styl'
    .recommend-title
        margin-top: .2rem
        line-height: .8rem
        background: #ee
        text-indent: .2rem
    .item
        overflow: hidden
        display: flex
        height: 1.9rem
        .item-img
            width: 1.7rem
            height: 1.7rem
            padding: .1rem
        .item-info
            flex: 1
            padding: .1rem
            min-width: 0
            .item-title
                line-height: .54rem
                font-size: .32rem
                ellipsis()
            .item-desc
                line-height: .4rem
                color: #ccc
                ellipsis()
            .item-button
                line-height: .44rem
                margin-top: .16rem
                background: #ff9300
                padding: 0 .2rem
                border-radius: .06rem
                color: #fff
</style>
