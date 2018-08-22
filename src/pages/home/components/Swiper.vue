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
                imgUrl: "http://img1.qunarzz.com/piao/fusion/1808/5e/514ce60160e62602.jpg_750x200_9b0074e2.jpg"
            }, {
                id: '0002',
                imgUrl: "http://img1.qunarzz.com/piao/fusion/1807/66/e5a5cec881702f02.jpg_750x200_67bb5691.jpg"
            }, {
                id: '0003',
                imgUrl: "http://img1.qunarzz.com/piao/fusion/1806/ae/2f9a9f0bbc30e102.jpg_750x200_75b6a866.jpg"
            }, {
                id: '0004',
                imgUrl: "http://img1.qunarzz.com/piao/fusion/1808/ad/1d2e0030d4ff7302.jpg_750x200_bf5a325d.jpg"
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
