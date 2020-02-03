<template>
    <div>
        <div class="recommend-title">周末去哪儿</div>
        <ul>
            <li
                class="item border-bottom"
                v-for="item of recommendList"
                :key="item.id"
            >
                <div class="item-img-wrapper">
                    <img class="item-img" :src="item.imgUrl" />
                </div>
                <div class="item-info">
                    <p class="item-title">{{ item.title }}</p>
                    <p class="item-desc">{{ item.desc }}~</p>
                </div>
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    name: "HomeWeekend",
    data() {
        return {
            recommendList: [
                {
                    id: "0001",
                    imgUrl:
                        "http://img1.qunarzz.com/sight/source/1511/ea/7f43191b747bb9.jpg_r_640x214_f58e829d.jpg",
                    title: "上海泡汤胜地",
                    desc:
                        "上海的朋友总会问，哪里可以泡温泉，哪里的温泉好呢？这里有最好最全的上海温泉"
                },
                {
                    id: "0002",
                    imgUrl:
                        "http://img1.qunarzz.com/sight/source/1505/7d/df6ff468331c43.jpg_r_640x214_1f3783d0.jpg",
                    title: "上海必打卡",
                    desc: "中西合璧，现代和传统各有各的精彩"
                },
                {
                    id: "0003",
                    imgUrl:
                        "http://img1.qunarzz.com/sight/source/1505/7b/2a6b0ce087f0e5.jpg_r_640x214_5c76b115.jpg",
                    title: "情迷博物馆",
                    desc:
                        "走进艺术殿堂，电影博物馆生动演绎着电影人和电影背后的故事，你不想知道吗~"
                }
            ]
        }
    }
}
</script>

<style lang="stylus" scoped>
@import '~styles/mixins.styl';

.recommend-title {
  margin-top: 0.2rem;
  line-height: 0.8rem;
  background: #eee;
  text-indent: 0.2rem;
}

.item-img-wrapper {
  overflow: hidden;
  height: 0;
  padding-bottom: 33.9%;

  .item-img {
    width: 100%;
  }
}

.item-info {
  padding: 0.1rem;
  min-width: 0;

  .item-title {
    line-height: 0.54rem;
    font-size: 0.32rem;
    ellipsis();
  }

  .item-desc {
    line-height: 0.4rem;
    color: #ccc;
    ellipsis();
  }
}
</style>
