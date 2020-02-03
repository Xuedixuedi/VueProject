<template>
    <div class="wrapper">
        <swiper :options="swiperOption">
            <!-- slides -->
            <swiper-slide v-for="item of swiperList" :key="item.id">
                <img class="swiper-img" :src="item.imgUrl" />
            </swiper-slide>

            <!-- Optional controls -->
            <div class="swiper-pagination" slot="pagination"></div>
        </swiper>
    </div>
</template>

<script>
export default {
    name: "HomeSwiper",
    data() {
        return {
            swiperOption: {
                pagination: ".swiper-pagination",
                loop: true
            },
            swiperList: [
                {
                    id: "0001",
                    imgUrl:
                        "http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20198/da3db1d9761f8984fd9c84c4eccf93ee.jpg_750x200_b7f8686a.jpg"
                },
                {
                    id: "0002",
                    imgUrl:
                        "http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20199/bc504af704ef02fbc0455fdbab8635ee.jpg_750x200_fa9cad2a.jpg"
                },
                {
                    id: "0003",
                    imgUrl:
                        "http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20199/249dfa53de67b8824a96f9821e58f30d.jpg_750x200_48bf24d9.jpg"
                }
            ]
        }
    }
}
</script>

<style lang="stylus" scoped>
.wrapper>>>.swiper-pagination-bullet-active {
  background: #ffffff;
}

.wrapper {
  overflow: hidden;
  width: 100%;
  height: 0;
  padding-bottom: 26.9%;
  background: #eeeeee;

  .swiper-img {
    width: 100%;
  }
}
</style>
