<template>
    <div class="container">
      <div>
        <b-card overlay img-src="//cdn2.jianshu.io/assets/web/recommend-author-03cc8798d5cc3f986e49cbcb2eb63079.png">
          <p class="help">
            如何成为签约作者
          </p>
        </b-card>
      </div>
      <b-row class="col-xs-8">
      <b-col cols="4" v-for="user in userList" :key="user.id" class="wrap">
        <b-navbar>
          <router-link :to="'/u/'+user.id">
            <img class="avatar" :src="user.url">
            <h4 class="name">{{user.author}}</h4>
            <p class="description">{{user.description}}</p>
            <a class="follow"><span>关注</span></a>
            <div class="meta">最近更新</div>
            <div>
              <a>【奇幻】唐朝那些猫事</a>
              <a>【奇幻】唐朝那些猫事</a>
              <a>【奇幻】唐朝那些猫事</a>
            </div>
          </router-link>
        </b-navbar>
      </b-col>
      </b-row>
    </div>
</template>

<script>
    export default {
        name: "Users",
      data(){
          return{
            userList:[
              {
                "id":1,
                "url":"//upload.jianshu.io/users/upload_avatars/5205317/1179d71b-e7c6-4023-89e8-bba25f88272b.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/180/h/180",
                "author":"遛遛心情的溜妈",
                "description":"溜爸，简书签约作者，舞枪弄棒、舞文弄墨的计算..."
              },
              {
                "id":2,
                "url":"//upload.jianshu.io/users/upload_avatars/2587459/0c7e061f-e78e-4b09-b511-340846c4ea0f.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/180/h/180",
                "author":"穿着prada挤地铁",
                "description":"只写好玩的都市生活版权合作事宜请联系简..."
              },
              {
                "id":3,
                "url":"//upload.jianshu.io/users/upload_avatars/3884693/b425c707-d998-46a6-98b1-9b1e241513c3.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/96/h/96/format/webp",
                "author":"遛遛心情的溜妈",
                "description":"溜爸，简书签约作者，舞枪弄棒、舞文弄墨的计算..."
              },
              {
                "id":4,
                "url":"//upload.jianshu.io/users/upload_avatars/3292545/78f2855a-80fd-419a-9fb2-1aeed39690f0.png?imageMogr2/auto-orient/strip|imageView2/1/w/180/h/180",
                "author":"遛遛心情的溜妈",
                "description":"溜爸，简书签约作者，舞枪弄棒、舞文弄墨的计算..."
              },
              {
                "id":5,
                "url":"//upload.jianshu.io/users/upload_avatars/11557689/ed2ea7f3-9d7d-41fc-a05a-daebb8097b0c.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/180/h/180",
                "author":"遛遛心情的溜妈",
                "description":"溜爸，简书签约作者，舞枪弄棒、舞文弄墨的计算..."
              }
            ],
          }
      }
    }
</script>

<style scoped>
  .col-xs-8{
    position: relative;
    min-height: 1px;
    padding-left: 15px;
    padding-right: 15px;
  }
  .follow{
    width: 100px;
    border-color: #42c02e;
    padding: 8px 22px;
    font-size: 16px;
    font-weight: 400;
    line-height: normal;
    border-radius: 40px;
    color: #fff;
    background-color: #42c02e;
  }
  .description{
    margin: 0 auto 10px;
    max-width: 180px;
  }
  .name{
    font-size: 21px;
    font-weight: 700;
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
  }
  .avatar{
    border-radius: 40px;
  }
  .wrap{
    height: 320px;
    margin-top: 80px;
    padding: 0 20px;
    border: 1px solid #e6e6e6;
    border-radius: 4px;
    background-color: hsla(0,0%,71%,.1);
    transition: .2s ease;
    -webkit-transition: .2s ease;
  }
.help{
  position: absolute;
  right: 30px;
  top: 68px;
  color: #fff;
}
</style>
