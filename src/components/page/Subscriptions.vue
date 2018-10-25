<template>
  <div>
    <div class="aside">
      <a>全部关注</a>
      <div class="guanzhu">
        <img  class="avatar" src="//cdn2.jianshu.io/assets/web/addfollow-fc392ec918dda9d19818181ca42d2d7e.png">
        <span>添加关注</span>
      </div>
    </div>
    <div class="col-xs-16 col-xs-offset-8 main">
    <b-card no-body>
      <b-tabs card v-model="tabIndex" class="trigger-menu">
        <b-tab title="全部推荐" :title-link-class="linkClass(0)">

        </b-tab>
        <b-tab title="推荐作者" :title-link-class="linkClass(1)">
           <b-col  v-for="users in userList" :key="users.id">
             <a class="btn-success"><span>关注</span></a>
            <img class="avatar" :src="users.url">
            <a>{{users.author}}</a>
            <p>{{users.content}}</p>
          </b-col>
          <a class="load-more">查看更多</a>
        </b-tab>
        <b-tab title="推荐专题" :title-link-class="linkClass(2)">
          <b-col v-for="course in courseList" :key="course.id">
            <b-navbar>
              <img style=";float:left;width: 52px;height:52px" :src="course.url">
              <div class="info">
                <a class="btn"><span>关注</span></a>
                <p class="name">{{course.courseName}}</p>
                <p style="font-size: 12px;color: #969696">欢迎关注公众号简宝玉( 公众号ID : jianshu4321 ...</p>
                <span>128.9K篇文章 · 1633.7K人关注</span>
              </div>
            </b-navbar>
            <a class="load-more">查看更多</a>
          </b-col>
        </b-tab>
      </b-tabs>
    </b-card>
    </div>
  </div>
</template>

<script>
    export default {
        name: "Subscriptions",
      data () {
        return {
          tabIndex: 0,
          courseList:[
                {
                  "id":1,
                  "url":"//upload.jianshu.io/collections/images/283250/%E6%BC%AB%E7%94%BB%E4%B8%93%E9%A2%98.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/64/h/64",
                  "courseName":"手绘"
                },
                {
                  "id":2,
                  "url":"//upload.jianshu.io/collections/images/4/sy_20091020135145113016.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/64/h/64",
                  "courseName":"读书"
                },
                {
                  "id":3,
                  "url":"//upload.jianshu.io/collections/images/21/20120316041115481.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/64/h/64",
                  "courseName":"简书电影"
                },
                {
                  "id":4,
                  "url":"//upload.jianshu.io/collections/images/76/12.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/64/h/64",
                  "courseName":"自然科普"
                },
                {
                  "id":5,
                  "url":"//upload.jianshu.io/collections/images/83/1.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/64/h/64",
                  "courseName":"摄影"
                },
                {
                  "id":6,
                  "url":"//upload.jianshu.io/collections/images/4/sy_20091020135145113016.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/64/h/64",
                  "courseName":"读书"
                },
                {
                  "id":7,
                  "url":"//upload.jianshu.io/collections/images/14/6249340_194140034135_2.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/64/h/64",
                  "courseName":"@IT·互联网"
                },
          ],
          userList:[
            {
              "id":1,
              "url":"//upload.jianshu.io/users/upload_avatars/3884693/b425c707-d998-46a6-98b1-9b1e241513c3.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/96/h/96/format/webp",
              "author":"王诗翔",
              "content":"合抱之木，生于毫末,九层之台，起于垒土,千里之行，始于足下"
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
  .btn-success{
    border-radius: 40px;
    color: #fff;
    background-color: #42c02e;
    border-color: #42c02e;
    float: right;
  }
  span{
    margin-left: 2px;
    display: inline;
  }
  .btn{
    float: right;
    padding: 8px 0;
    margin-top: 5px;
    width: 100px;
  }
  .info{
    padding-left: 64px;
    padding-right: 120px;
    line-height: normal;
    min-height: 50px;
  }
  .name{
    margin: 0 0 5px;
    font-size: 15px;
    font-weight: 700;
    color: #333;
    display: block;
  }
  .col-xs-offset-8 {
    margin-left: 25%;
  }
  .avatar{
    width: 40px;
    height: 40px;
    margin-right: 4px;
    display: inline-block;
  }
  .guanzhu{
    line-height: 20px;
    text-align: -webkit-match-parent;
    box-sizing: border-box;
  }
  .aside{
    position: fixed;
    top: 0;
    bottom: 0;
    margin: 86px 0 0;
    padding: 0 0 30px;
    width: 280px;
    overflow: auto;
    border-right: 1px solid #f0f0f0;
  }
.trigger-menu{
  margin-bottom: 20px;
  font-size: 15px;
  list-style: none;
}
  p{
    display: block;
    -webkit-margin-before: 1em;
    -webkit-margin-after: 1em;
    -webkit-margin-start: 0px;
    -webkit-margin-end: 0px;
  }
</style>
