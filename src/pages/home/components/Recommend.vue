<template>
    <div>
        <div class="recommend-title">热销推荐</div>
        <ul>
            <li
                class="item border-bottom"
                v-for="item of recommendList"
                :key="item.id"
            >
                <img class="item-img" :src="item.imgUrl" />
                <div class="item-info">
                    <p class="item-title">{{ item.title }}</p>
                    <p class="item-desc">{{ item.desc }}~</p>
                    <button class="item-button">查看详情</button>
                </div>
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    name: "HomeRecommend",
    data() {
        return {
            recommendList: [
                {
                    id: "0001",
                    imgUrl:
                        "http://img1.qunarzz.com/sight/p0/1607/7c/7cda8b6782dabd80b4.img.jpg_200x200_2039e660.jpg",
                    title: "周末亲子爱玩",
                    desc:
                        "走进自然或玩转乐园，感知大千世界，游乐项目惊险刺激，特色表演异彩纷呈，等你们~"
                },
                {
                    id: "0002",
                    imgUrl:
                        "http://img1.qunarzz.com/tuan/team2/1507/2c/83e0e0e7ae082a.jpg_200x200_6d7378b2.jpg",
                    title: "上海必打卡",
                    desc: "中西合璧，现代和传统各有各的精彩"
                },
                {
                    id: "0003",
                    imgUrl:
                        "http://img1.qunarzz.com/sight/p0/1803/26/2645c1b2ee526285a3.water.jpg_200x200_d5b170d5.jpg",
                    title: "上海城市观光",
                    desc:
                        "来这里寻找你所不认识的魔都 ，感受云端漫步，品味老上海风情，享受休闲时光"
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

.item {
  overflow: hidden;
  display: flex;
  height: 1.9rem;

  .item-img {
    width: 1.7rem;
    height: 1.7rem;
    padding: 0.1rem;
  }

  .item-info {
    flex: 1;
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

    .item-button {
      line-height: 0.44rem;
      margin-top: 0.16rem;
      background: #ff9300;
      padding: 0.02rem;
      border-radius: 0.09rem;
      color: #fff;
    }
  }
}
</style>
