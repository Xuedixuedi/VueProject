<template>
    <div class="container" @click="handelGallaryClick">
        <div class="wrapper">
            <swiper :options="swiperOptions">
                <swiper-slide v-for="(item, index) in imgs" :key="index">
                    <img class="gallary-img" :src="item" />
                </swiper-slide>
                <div class="swiper-pagination" slot="pagination"></div>
            </swiper>
        </div>
    </div>
</template>

<script>
export default {
    name: "CommonGallary",
    props: {
        imgs: {
            type: Array,
            default() {
                return [
                    // "http://img1.qunarzz.com/sight/p0/1803/9d/9d862d8166170089a3.img.jpg_350x240_822366e0.jpg",
                    // "http://img1.qunarzz.com/sight/p0/1803/f0/f0592ef10e644699a3.img.jpg_350x240_a9ce1337.jpg"
                ]
            }
        }
    },
    data() {
        return {
            swiperOptions: {
                pagination: ".swiper-pagination",
                paginationType: "fraction",
                observeParents: true,
                observer: true
            }
        }
    },
    methods: {
        handelGallaryClick() {
            this.$emit("close")
        }
    }
}
</script>

<style lang="stylus" scoped>
.container >>> .swiper-container {
  overflow: inherit;
}

.container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  z-index: 99;
  position: fixed;
  left: 0;
  right: 0;
  top: 0;
  bottom: 0;
  background: #000;

  .wrapper {
    height: 0;
    width: 100%;
    padding-bottom: 100%;

    .gallary-img {
      width: 100%;
    }

    .swiper-pagination {
      color: #ffffff;
      bottom: -1rem;
    }
  }
}
</style>