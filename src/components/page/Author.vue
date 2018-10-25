<template>
    <div class="container">
      <b-row>
      <b-col cols="8">
        <a class="avatar">
          <b-img rounded="circle" width="80" height="80" src="//cdn2.jianshu.io/assets/default_avatar/7-0993d41a595d6ab6ef17b19496eb2f21.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/120/h/120"/>
        </a>
        <div class="title">
          <a class="name" >落幕晟伤</a>
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
        <ul class="list">
          <li><a><img style="width: 20px;height: 20px" src="//upload.jianshu.io/user_badge/ac944899-bf5f-40df-b265-7d947fadd946">生活达人</a></li>
          <li><a><img style="width: 20px;height: 20px" src="//upload.jianshu.io/user_badge/ac944899-bf5f-40df-b265-7d947fadd946">儿童故事优秀作者</a></li>
          <li><a><img style="height: 20px;width: 20px" src="////upload.jianshu.io/user_badge/48d31e61-a03c-4506-81a2-d224ac0a2d8b">简书版权</a></li>
          <li><a><img style="height: 20px;width: 20px" src="//cdn2.jianshu.io/assets/badges/signed-9702260821906f0d953eab67a29f8e7a2d2e3d20960576347591283a3fbfd867.png">简书签约作者</a></li>
        </ul>
        <div class="title">个人介绍</div>
        <div class="">
          <p>溜爸，简书签约作者，舞枪弄棒、舞文弄墨的计算机工程师，梦想老婆孩子热炕头上写故事。<br>溜妈，溜溜的大奶牛，北师大教育学硕士牌的，美国认证正面管教讲师、鼓励咨询师，一点一滴分享育儿经验。<br>微信公号：遛遛心情 个人微信：xi13718906914<br>转载声明：转载分为两种，一是有偿转载，即付给作者相应的稿酬；二是无偿转载，需注明作者为简书签约作者，并在文章后放简书二维码。除此之外的转载都会被视为侵权，简书不惜一切追究侵权责任。关于转载事宜，请联系简书版权经理“sherry时芽”（简信即可）。</p>
        </div>
        <div class="user-action">
          <a>加入黑名单</a>.
          <a>举报用户</a>
        </div>
      </b-col>
      </b-row>
    </div>
</template>

<script>
    export default {
        name: "Author",
      data(){
          return{
            tableIndex:0,
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
  .title{
    padding: 5px 0 0 100px;
  }
  .user-action{
    padding-bottom: 20px;
    color: #969696;
  }
  .list{
    margin-bottom: 16px;
    padding-bottom: 16px;
    list-style: none;
    border-bottom: 1px solid #f0f0f0;
    clear: both;
  }
</style>
