<template>
    <div class="wrapper">
        <swiper :options="swiperOption">
          <!-- slides -->
          <swiper-slide v-for="item of swiperList" :key="item.id">
              <img class="swiper-img" :src="item.imgUrl" />
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
                imgUrl: "https://m.360buyimg.com/mobilecms/s750x366_jfs/t23185/303/2268048621/426877/b0ab0a91/5b7a36a4Ned6def2c.jpg!cr_1125x549_0_72!q70.jpg.dpg"
            }, {
                id: '0002',
                imgUrl: "https://img1.360buyimg.com/da/s750x366_jfs/t25615/287/616242820/100113/bd8b5722/5b763b70N7ab570bd.jpg!cr_1125x549_0_72.dpg"
            }, {
                id: '0003',
                imgUrl: "https://img1.360buyimg.com/da/s750x366_jfs/t25387/228/752902205/83028/c185d78/5b7a34a4N19d040fe.jpg!cr_1125x549_0_72.dpg"
            }, {
                id: '0004',
                imgUrl: "https://m.360buyimg.com/mobilecms/s750x366_jfs/t20029/272/1765431541/135543/fbf22a8b/5b25a7d0Ncdb4f0f3.jpg!cr_1125x549_0_72!q70.jpg.dpg"
            }],
        }
    }
}
</script>

<style lang="stylus" scoped>
    .wrapper >>> .swiper-pagination-bullet
        background: #fff !important
    .wrapper
        /* overflow: hidden
        width: 100%
        height: 100%
        padding-bottom: 31.25% */
        background: #eee
        .swiper-img
            width: 100%
</style>
