<template>
  <div class="app">
    <van-swipe
      class="my-swipe"
      :autoplay="3000"
      indicator-color="white"
      width="100%"
    >
      <van-swipe-item>
        <van-image
          width="100%"
          height="100%"
          src="https://fastly.jsdelivr.net/npm/@vant/assets/cat.jpeg"
        />
      </van-swipe-item>
      <van-swipe-item>
        <van-image
          width="100%"
          height="100%"
          src="https://fastly.jsdelivr.net/npm/@vant/assets/cat.jpeg"
        />
      </van-swipe-item>
      <van-swipe-item>
        <van-image
          width="100%"
          height="100%"
          src="https://fastly.jsdelivr.net/npm/@vant/assets/cat.jpeg"
        />
      </van-swipe-item>
      <van-swipe-item>
        <van-image
          width="100%"
          height="100%"
          src="https://fastly.jsdelivr.net/npm/@vant/assets/cat.jpeg"
        />
      </van-swipe-item>
      <van-swipe-item>
        <van-image
          width="100%"
          height="100%"
          src="https://fastly.jsdelivr.net/npm/@vant/assets/cat.jpeg"
        />
      </van-swipe-item>
    </van-swipe>

    <div id="index_hot">
      <div id="index_title">
        <p class="title">精品分类</p>
      </div>
      <div id="index_hot-list">
        <van-row gutter="30">
          <van-col span="12">
            <div>免流教程</div>
          </van-col>
          <van-col span="12">
            <div>免流混淆</div>
          </van-col>
          <van-col span="12">
            <div>v2ray、clash下载及使用</div>
          </van-col>
          <van-col span="12">
            <div>阿里云盘影视</div>
          </van-col>
        </van-row>
      </div>
    </div>

    <van-tabs v-model="active" color="#fb6c28">
      <van-tab title="最新文章">
        <div class="index_item" @click="goArticle">
          <div class="bg"></div>
          <div class="js">
            <div class="js_header">教你利用阿里云盘在线观看各大影视资源</div>
            <div class="js_meta">
              <div class="js_rq">2022-05-09</div>
              <div class="js_ly">阿里云盘影视</div>
            </div>
          </div>
        </div>
      </van-tab>
      <van-tab title="热门文章"></van-tab>
    </van-tabs>
  </div>
</template>

<script>
export default {
  setup() {
    const activeName = ref("a");
    return { activeName };
  },
  methods: {
    goArticle() {
      this.$router.push("/article");
    },
  },
};
</script>

<style scoped>
.app {
  margin-top: 46px;
      background: rgb(0 0 0 / 0%);
}
div {
  font-family: "Joe Font", "Helvetica Neue", Helvetica, "PingFang SC",
    "Hiragino Sans GB", "Microsoft YaHei", "微软雅黑", Arial, "sans-serif";
}
.my-swipe .van-swipe-item {
  width: 100%;
  height: 220px;
  text-align: center;
}
.van-swipe__indicators {
  left: 90%;
}
#index_hot {
  width: 96%;
  height: 210px;
  margin: 0px 2%;
  margin-bottom: 20px;
}
.title {
  padding: 0.266667rem 0.24rem;
  margin: 0 0 0.24rem 0;
  color: #fb6c28;
  font-size: 15px;
  font-weight: 500;
  text-align: left;
  height: 45px;
  line-height: 50px;
  border-bottom: 1px solid #ebeef5;
}
.van-col {
  background-size: 95%;
  background-repeat: no-repeat;
  background-position: center;
  height: 70px;
  border-radius: 10px;
  overflow: hidden;
  margin: 5px 0px;
}
.van-col:nth-child(1) {
  background-image: url(https://cdn.jsdelivr.net/gh/qinhua/halo-theme-joe2.0@1.0.8/source/img/hot_cover1.jpg);
}
.van-col:nth-child(2) {
  background-image: url(https://cdn.jsdelivr.net/gh/qinhua/halo-theme-joe2.0@1.0.8/source/img/hot_cover2.jpg);
}
.van-col:nth-child(3) {
  background-image: url(https://cdn.jsdelivr.net/gh/qinhua/halo-theme-joe2.0@1.0.8/source/img/hot_cover3.jpg);
}
.van-col:nth-child(4) {
  background-image: url(https://cdn.jsdelivr.net/gh/qinhua/halo-theme-joe2.0@1.0.8/source/img/hot_cover4.jpg);
}
.van-tab .van-tabs__line {
  width: 70px;
}
.van-tab__pane {
  width: 96%;
  height: 300px;
  margin: 0px 2%;
}
.index_item {
  width: 100%;
  height: 90px;
  padding: 10px 0px;
  border-bottom: 1px solid #d4d4d4;
}
.bg {
  width: 35%;
  height: 90px;
  background-image: url(https://tu.ltyuanfang.cn/api/fengjing.php?_r=33);
  background-size: cover;
  background-position: center;
  border-radius: 5px;
}
.js {
  margin-left: 3%;
  width: 62%;
  height: 90px;
  font-size: 15px;
}
.index_item div {
  float: left;
}
.js_header {
  text-align: left;
  margin-bottom: 30px;
}
.js_rq {
  color: #909399;
  font-size: 13px;
  margin-top: 2px;
}
.js_ly {
  color: #909399;
}
#index_hot-list .van-row .van-col div {
  font-size: 14px;
  color: white;
  width: 110%;
  height: 15px;
  line-height: 15px;
  overflow: hidden;
  margin-top: 19%;
}
</style>
