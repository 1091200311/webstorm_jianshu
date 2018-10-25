<template>
  <div class="container">
    <b-row>
      <b-col cols="8" class="col-xs-16 main">
        <a class="avatar">
          <b-img rounded="circle" width="80" height="80" src="//cdn2.jianshu.io/assets/default_avatar/7-0993d41a595d6ab6ef17b19496eb2f21.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/120/h/120"/>
        </a>
        <div class="title">
          <a class="name">落幕晟伤</a>
        </div>
        <div class="info">
          <div>
            <b-nav>
              <b-nav-item href="/users/7b9cc26fb573/following"><p>0</p>关注</b-nav-item>
              <b-nav-item><p>0</p>粉丝</b-nav-item>
              <b-nav-item><p>9</p>文章</b-nav-item>
              <b-nav-item><p>4811</p>字数</b-nav-item>
              <b-nav-item><p>0</p>收藏或喜欢</b-nav-item>
            </b-nav>
          </div>
        </div>
        <b-card no-body class="trigger-menu">
          <b-tabs card v-model="tabIndex">
            <b-tab title="文章" :title-link-class="linkClass(0)">
              <b-col  v-for="articles in articleList" :key="articles.id" style="border-bottom: 1px solid #f0f0f0;">
                <a class="title">{{articles.title}}</a>
                <p class="abstract">{{articles.content}}</p>
                <div></div>
              </b-col>
            </b-tab>
            <b-tab title="动态" :title-link-class="linkClass(1)">
            </b-tab>
            <b-tab title="最新评论" :title-link-class="linkClass(2)">
            </b-tab>
            <b-tab title="热门" :title-link-class="linkClass(3)">
            </b-tab>
          </b-tabs>
        </b-card>
      </b-col>
      <b-col>
        <div style="border-bottom: 1px solid #f0f0f0;">个人介绍</div>
        <div  class="list" style="padding-bottom: 6px;border-bottom: 1px solid #f0f0f0;">
          <span>我关注的专题/连载/文集</span>
          <span>我喜欢的文章</span>
        </div>
        <div class="title">我的文集</div>
        <b-list-group class="list">
          <b-list-group-item class="name">Android移动应用开发</b-list-group-item>
          <b-list-group-item class="name">SpringBoot</b-list-group-item>
        </b-list-group>
      </b-col>
    </b-row>
  </div>
</template>

<script>
    export default {
        name: "User",
      data () {
        return {
          tabIndex: 0,
          articleList:[
            {
              "id":1,
              "title":"微信小程序模板消息定时推送，只需要简单三步就好",
              "content": "最近更新了创建推送API接口的模块，所以你要是想做一个定时推送微信小程序模板消息的功能，只需要简单的三步就好！ 1. 添加应用 首先进入vPus..."
            },
            {
              "id":2,
              "title":"微信小程序模板消息定时推送，只需要简单三步就好",
              "content": "最近更新了创建推送API接口的模块，所以你要是想做一个定时推送微信小程序模板消息的功能，只需要简单的三步就好！ 1. 添加应用 首先进入vPus..."
            },
            {
              "id":3,
              "title":"微信小程序模板消息定时推送，只需要简单三步就好",
              "content": "最近更新了创建推送API接口的模块，所以你要是想做一个定时推送微信小程序模板消息的功能，只需要简单的三步就好！ 1. 添加应用 首先进入vPus..."
            }
          ]
        }
      },
      methods: {
        linkClass (idx) {
          if (this.tabIndex === idx) {
            return ['bg-primary', 'text-light']
          } else {
            return ['bg-light', 'text-info']
          }
        }
      }
    }
</script>

<style scoped>
  .list{
    margin-bottom: 16px;
    padding-bottom: 16px;
    list-style: none;
    border-bottom: 1px solid #f0f0f0;
    clear: both;
  }
  .name{
    position: relative;
    max-width: 236px;
    vertical-align: middle;
    top: 1px;
    font-size: 14px;
    color: #333;
  }
  .abstract{
    margin: 0 0 8px;
    font-size: 13px;
    line-height: 24px;
    color: #999;
  }
  p{
    margin-bottom: -3px;
    font-size: 15px;
    color: #333;
  }
  a{
    cursor: pointer;
  }
  .name{
    display: inline;
    font-size: 21px;
    font-weight: 700;
    vertical-align: middle;
  }
  .title{
    padding: 5px 0 0 100px;
  }
  .col-xs-16 {
    width: 66.66667%;
  }
.main{
  margin-top: 20px;
  width: 80px;
  height: 80px;
}
  .avatar{
    float: left;
    width: 80px;
    height: 80px;
    margin-left: -2px;
  }
  .info{
    margin-top: 5px;
    padding-left: 100px;
    font-size: 14px;
  }
</style>
