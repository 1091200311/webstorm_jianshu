<template>
  <b-row>
    <b-col cols="8">
      <v-carousel></v-carousel>
      <v-collection></v-collection>
      <b-col  v-for ="articles in articleList" :key="articles.id" class="have-img">
        <img class="wrap-img" :src="articles.url">
        <a class="title">{{articles.title}}</a>
        <p class="abstract">{{articles.content}}</p>
        <div></div>
      </b-col>
    </b-col>
    <b-col>
      <b-nav vertical class="w-25">
        <b-nav-item><img src="//cdn2.jianshu.io/assets/web/banner-s-3-7123fd94750759acf7eca05b871e9d17.png" style="width: 250px"></b-nav-item>
        <b-nav-item><img src="//cdn2.jianshu.io/assets/web/banner-s-4-b70da70d679593510ac93a172dfbaeaa.png" style="width: 250px"></b-nav-item>
        <b-nav-item><img src="//cdn2.jianshu.io/assets/web/banner-s-7-1a0222c91694a1f38e610be4bf9669be.png" style="width: 250px"></b-nav-item>
        <b-nav-item><img src="//cdn2.jianshu.io/assets/web/banner-s-5-4ba25cf5041931a0ed2062828b4064cb.png" style="width: 250px"></b-nav-item>
        <b-nav-item><img src="//cdn2.jianshu.io/assets/web/banner-s-6-c4d6335bfd688f2ca1115b42b04c28a7.png" style="width: 250px"></b-nav-item>
      </b-nav>
      <a class="download">
        <img class="qrcode" src="//cdn2.jianshu.io/assets/web/download-index-side-qrcode-cb13fc9106a478795f8d10f9f632fccf.png">
      </a>
      <div class="info">
        <div class="title">下载简书手机App</div>
        <div class="description">随时随地创作和发现内容</div>
      </div>
      <div class="title">
        <span style="font-size: 14px">推荐作者</span>
        <a class="change">换一批</a>
        <b-col  v-for="users in userList" :key="users.id">
          <img class="avatar" :src="users.url">
          <a class="title">{{users.author}}</a>
          <p class="abstract">{{users.content}}</p>
        </b-col>
        <router-link class="find-more" to="/users">查看全部</router-link>
      </div>
    </b-col>
  </b-row>
</template>

<script>
  import vCarousel from '../common/Carousel';
  import vCollection from '../common/Collection';

  export default {
    name: "Index",
    components: {
      vCarousel,
      vCollection
    },
    data(){
      return{
        userList:[
          {
            "id":1,
            "url":"//upload.jianshu.io/users/upload_avatars/3884693/b425c707-d998-46a6-98b1-9b1e241513c3.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/96/h/96/format/webp",
            "author":"王诗翔",
            "content":"写了434.5k字 · 1.7k喜欢"
          },
          {
            "id":2,
            "url":"//upload.jianshu.io/users/upload_avatars/3884693/b425c707-d998-46a6-98b1-9b1e241513c3.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/96/h/96/format/webp",
            "author":"王诗翔",
            "content":"写了434.5k字 · 1.7k喜欢"
          },
          {
            "id":3,
            "url":"//upload.jianshu.io/users/upload_avatars/3884693/b425c707-d998-46a6-98b1-9b1e241513c3.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/96/h/96/format/webp",
            "author":"王诗翔",
            "content":"写了434.5k字 · 1.7k喜欢"
          },
          {
            "id":4,
            "url":"//upload.jianshu.io/users/upload_avatars/3884693/b425c707-d998-46a6-98b1-9b1e241513c3.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/96/h/96/format/webp",
            "author":"王诗翔",
            "content":"写了434.5k字 · 1.7k喜欢"
          },
          {
            "id":5,
            "url":"//upload.jianshu.io/users/upload_avatars/3884693/b425c707-d998-46a6-98b1-9b1e241513c3.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/96/h/96/format/webp",
            "author":"王诗翔",
            "content":"写了434.5k字 · 1.7k喜欢"
          }
        ],
        articleList:[
          {
            "id":1,
            "avatar":"//upload-images.jianshu.io/upload_images/10044645-f475d8cc57510b85.png?imageMogr2/auto-orient/strip|imageView2/1/w/300/h/240",
            "title":"微信小程序模板消息定时推送，只需要简单三步就好",
            "content": "最近更新了创建推送API接口的模块，所以你要是想做一个定时推送微信小程序模板消息的功能，只需要简单的三步就好！ 1. 添加应用 首先进入vPus..."
          },
          {
            "id":2,
            "avatar":"//upload-images.jianshu.io/upload_images/10044645-f475d8cc57510b85.png?imageMogr2/auto-orient/strip|imageView2/1/w/300/h/240",
            "title":"微信小程序模板消息定时推送，只需要简单三步就好",
            "content": "最近更新了创建推送API接口的模块，所以你要是想做一个定时推送微信小程序模板消息的功能，只需要简单的三步就好！ 1. 添加应用 首先进入vPus..."
          },
          {
            "id":3,
            "avatar":"//upload-images.jianshu.io/upload_images/10044645-f475d8cc57510b85.png?imageMogr2/auto-orient/strip|imageView2/1/w/300/h/240",
            "title":"微信小程序模板消息定时推送，只需要简单三步就好",
            "content": "最近更新了创建推送API接口的模块，所以你要是想做一个定时推送微信小程序模板消息的功能，只需要简单的三步就好！ 1. 添加应用 首先进入vPus..."
          }
        ]
      }
    }
  }
</script>
<style scoped>
  .have-img{
    min-height: 140px;
    border-bottom: 1px solid #f0f0f0;
  }
  .abstract{
    margin: 0 0 8px;
    font-size: 13px;
    line-height: 24px;
    color: #999;
  }
  .wrap-img{
    position: absolute;
    top: 50%;
    margin-top: -60px;
    right: 0;
    width: 125px;
    height: 100px;
  }
  p{
    margin-top: 2px;
    font-size: 12px;
    color: #969696;
  }
  .change{
    float: right;
    display: inline-block;
    font-size: 14px;
    color: #969696;
  }
  .description{
    margin-top: 4px;
    font-size: 13px;
    color: #999;
  }
  .title{
    font-size: 15px;
    color: #333;
  }
  .info{
    display: inline-block;
    vertical-align: middle;
    margin-left: 7px;
  }
  .qrcode{
    width: 45px;
    height: 45px;
    opacity: .85;
  }
.download{
  margin-bottom: 100px;
  padding: 10px 22px;
  width: 100%;
  border: 1px solid #f0f0f0;
  border-radius: 6px;
  background-color: #fff;
}
  .find-more{
    position: absolute;
    padding: 7px 7px 7px 12px;
    left: 0;
    width: 100%;
    font-size: 13px;
    color: #787878;
    background-color: #f7f7f7;
    border: 1px solid #dcdcdc;
    border-radius: 4px;
  }
  .avatar{
    float: left;
    width: 48px;
    height: 48px;
    margin-right: 10px;
  }
</style>
