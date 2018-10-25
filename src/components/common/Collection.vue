<template>
  <div>
    <b-row class="recommend-collection">
          <b-col cols="3" v-for="course in courseList" :key="course.id">
          <b-navbar>
            <router-link :to="'/c/'+course.id">
            <img style="width: 32px;height:32px" :src="course.url">
            <div class="name">

            {{course.courseName}}
            </div>
            </router-link>
          </b-navbar>
          </b-col>
      <router-link  class="more-hot-collection" to="/collections">更多精彩</router-link>
    </b-row>
  </div>
</template>

<script>
    export default {
        name: "Collection",
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
            },
            {
              "id":7,
              "url":"//upload.jianshu.io/collections/images/14/6249340_194140034135_2.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/64/h/64",
              "courseName":"@IT·互联网"
            },
          ]
        }
      }
    }
</script>

<style scoped>
  .more-hot-collection {
    display: inline-block;
    margin-top: 7px;
    font-size: 14px;
    color: #787878;
  }
  .name{
    display: inline-block;
    padding: 0 11px 0 6px;
    font-size: 14px;
  }
  .recommend-collection {
    margin-bottom: 20px;
  }
</style>
