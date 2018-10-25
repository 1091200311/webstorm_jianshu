<template>
  <div class="container">
    <b-row>
      <b-col cols="8"  class="col-xs-16 main">
        <b-media vertical-align="center" style="margin-bottom: 35px">
          <img :src="topic.topicUrl" class="avatar-collection"/>
          <h6 class="title">{{topic.topicName}}</h6>
          <p class="info">
            收藏了{{topic.articleCount}}篇文章,{{topic.fans}}关注
          </p>
          <a class="btn-hollow">关注</a>
          <div class="btn-hollow">
            投稿
          </div>
        </b-media>
        <b-card no-body>
          <b-tabs pills card>
            <b-tab title="最新评论">
            </b-tab>
            <b-tab title="最新收录">
            </b-tab>
            <b-tab title="热门">
            </b-tab>
          </b-tabs>
        </b-card>
      </b-col>
      <b-col>
        <div style="border-bottom: 1px solid #f0f0f0;">
        <p class="title">专题公告</p>
        <p>{{topic.articleList.summary}}</p>
          </div>
        <div class="share">
          <span>分享到</span>
        </div>
        <div >
          <p class="title">管理员</p>
          <div>
            <img  class="avatar" src="//upload.jianshu.io/users/upload_avatars/259/5210859b-fc54-4cf8-908f-830f0237926a.png?imageMogr2/auto-orient/strip|imageView2/1/w/96/h/96/format/webp">
            <a class="name">简书</a>
            <span class="tag">创建者</span>
            </div>
            <b-col v-for="users in userList" :key="users.id" class="list">
              <img class="avatar" :src="users.url">
              <a class="name">{{users.author}}</a>
            </b-col>
          <a class="check-more">展开更多</a>
        </div>
        <div class="title">推荐作者</div>
        <b-row class="list">
          <b-col v-for="users in userList" :key="users.id" class="list">
            <img class="list-avatar" :src="users.url">
          </b-col>
        </b-row>
        <div class="title">关注的人</div>
        <b-row class="list">
        <b-col v-for="users in userList" :key="users.id" class="list">
          <img class="list-avatar" :src="users.url">
        </b-col>
        </b-row>
      </b-col>
    </b-row>
  </div>

</template>

<script>
  export default {
    data() {
      return {
        id: this.$route.params.id,
        topic: {},
        articleList: [],
        fansList:[],
        userList:[
          {
            "id":1,
            "url":"//upload.jianshu.io/users/upload_avatars/3884693/b425c707-d998-46a6-98b1-9b1e241513c3.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/96/h/96/format/webp",
            "author":"王诗翔",
          },
          {
            "id":2,
            "url":"//upload.jianshu.io/users/upload_avatars/3884693/b425c707-d998-46a6-98b1-9b1e241513c3.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/96/h/96/format/webp",
            "author":"王诗翔",
          },
          {
            "id":3,
            "url":"//upload.jianshu.io/users/upload_avatars/3884693/b425c707-d998-46a6-98b1-9b1e241513c3.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/96/h/96/format/webp",
            "author":"王诗翔",
          },
          {
            "id":4,
            "url":"//upload.jianshu.io/users/upload_avatars/3884693/b425c707-d998-46a6-98b1-9b1e241513c3.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/96/h/96/format/webp",
            "author":"王诗翔",
          },
          {
            "id":5,
            "url":"//upload.jianshu.io/users/upload_avatars/3884693/b425c707-d998-46a6-98b1-9b1e241513c3.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/96/h/96/format/webp",
            "author":"王诗翔",
          }
        ],
      }
    },
    activated() {
      this.id = this.$route.params.id;
      console.log(this.id);
      if (this.id == 1) {
        var t = {
          "id": 1,
          "topicName": "读书",
          "topicUrl": "https://upload.jianshu.io/collections/images/83/1.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/64/h/64",
          "summary": "读书读书读书读书读书读书读书读书",
          "articleCount": 49535,
          "fans": 1601,
          "description":"fdfdf",
          "creator":"简书",
          "articleList":[
            {
              "id":1,
              "title":"测试文章",
              "summary":"测试文章测试文章测试文章测试文章测试文章...",
              "thumbnail":"1.png",
              "authorId":2,
              "nickname":"作者",
              "comments":1234,
              "likes":12
            }
          ],
          "fansList":[
            {
              "authorId":3,
              "avatar":"11.png"
            }
          ]
        };
        this.topic = t;
      } else {
        this.topic = {};
      }
    },
    computed: function () {
      return this.topic;
    }
  }
</script>

<style scoped>
  .list-avatar{
    margin-right: -10px;
    width: 32px;
    height: 32px;
  }
  check-more{
    color: #2f2f2f;
  }
  .tag{
    padding: 1px 3px;
    margin-left: 2px;
    border-radius: 3px;
    font-size: 12px;
    color: #969696;
    border: 1px solid #969696;
  }
  .name{
    position: relative;
    max-width: 236px;
    vertical-align: middle;
    top: 1px;
    font-size: 14px;
    color: #333;
  }
  .list{
    margin-bottom: 20px;
    padding-bottom: 10px;
    list-style: none;
    border-bottom: 1px solid #f0f0f0;
    clear: both;
  }
  .share{
    margin-bottom: 20px;
    padding-bottom: 20px;
    border-bottom: 1px solid #f0f0f0;
    line-height: 30px;
  }
  .btn-hollow{
    float: right;
    width: 90px;
    font-size: 13px;
    margin: -32px 20px 15px 10px;
    border: 1px solid rgba(59,194,29,.7);
    color: #42c02e!important;
  }
  .info{
    margin-top: 5px;
    padding-left: 100px;
    font-size: 14px;
  }
.avatar-collection{
  float: left;
  width: 80px;
  height: 80px;
}
  .title{
    padding: 5px 0 0 100px;
  }
  .col-xs-16 {
    width: 66.66667%;
  }
  .avatar{
    margin-right: 5px;
    width: 32px;
    height: 32px;
  }
</style>
