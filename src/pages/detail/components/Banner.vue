<template>
    <div>
        <div class="banner" @click="handleBannerClick">
            <img
                class="banner-img"
                src="http://img1.qunarzz.com/sight/p0/1803/9d/9d862d8166170089a3.img.jpg_350x240_822366e0.jpg"
            />
            <div class="banner-info">
                <div class="banner-title">景山公园(AAAA景区)</div>
                <div class="banner-number">
                    <span class="iconfont banner-icon">&#xe678;</span>19
                </div>
            </div>
        </div>
        <common-gallary
            :imgs="imgs"
            v-show="showGallary"
            @close="handleGallaryClose"
        ></common-gallary>
    </div>
</template>

<script>
import CommonGallary from "common/gallary/Gallary"
export default {
    name: "DetailBanner",
    data() {
        return {
            showGallary: false,
            imgs: [
                "http://img1.qunarzz.com/sight/p0/1803/9d/9d862d8166170089a3.img.jpg_350x240_822366e0.jpg",
                "http://img1.qunarzz.com/sight/p0/1803/f0/f0592ef10e644699a3.img.jpg_350x240_a9ce1337.jpg"
            ]
        }
    },
    components: {
        CommonGallary
    },
    methods: {
        handleBannerClick() {
            this.showGallary = true
        },
        handleGallaryClose() {
            this.showGallary = false
        }
    }
}
</script>

<style lang="stylus" scoped>
.banner {
  position: relative;
  overflow: hidden;
  height: 0;
  padding-bottom: 55%;

  .banner-img {
    width: 100%;
  }

  .banner-info {
    display: flex;
    position: absolute;
    left: 0;
    right: 0;
    bottom: 0;
    line-height: 0.6rem;
    color: #ffffff;
    background-image: linear-gradient(top, rgba(0, 0, 0, 0), rgba(0, 0, 0, 0.8));

    .banner-title {
      font-size: 0.32rem;
      padding: 0 0.2rem;
      flex: 1;
    }

    .banner-number {
      padding: 0 0.4rem;
      line-height: 0.36rem;
      height: 0.36rem;
      margin-top: 0.14rem;
      border-radius: 0.2rem;
      background: rgba(0, 0, 0, 0.8);
      font-size: 0.24rem;

      .banner-icon {
        font-size: 0.15rem;
      }
    }
  }
}
</style>
