<template>
  <div class="container">
    <div>
      <b-card overlay img -src="//cdn2.jianshu.io/assets/web/recommend-collection-58f8968955ecbeb8f8f3b4cd95ec76be.png">
        <p class="help">
          如何创建并玩转专题
        </p>
      </b-card>
    </div>
    <b-card no-body>
      <b-tabs pills card>
        <b-tab title="推荐">
          <b-row>
          <b-col cols="4" v-for="course in courseList" :key="course.id" class="wrap-content">
            <b-navbar>
              <router-link :to="'/c/'+course.id">
                <img class="avatar-collections" :src="course.url">
                <h4>{{course.courseName}}</h4>
                <p class="collections-description">欢迎关注公众号简宝玉( 公众号ID : jianshu4321 )后台...</p>
                <a class="btn-success"><span>关注</span></a>
              </router-link>
            </b-navbar>
          </b-col>
          </b-row>
        </b-tab>
        <b-tab title="热门">
        </b-tab>
        <b-tab title="城市">
        </b-tab>
        <b-tab title="校园">
        </b-tab>
      </b-tabs>
    </b-card>
  </div>
</template>

<script>
    export default {
        name: "Collections",
      data(){
        return{
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
            }
          ]
        }
      }
    }
</script>

<style scoped>
  .avatar-collections{
    width: 80px;
    height: 80px;
    margin: -40px 0 10px;
    display: inline-block;
    border: 1px solid #ddd;
    background-color: #fff;
  }
  .wrap-content{
    height: 280px;
  }
  .help{
    position: absolute;
    right: 30px;
    top: 68px;
    color: #fff;
  }
</style>
