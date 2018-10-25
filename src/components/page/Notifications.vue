<template>
  <div>
    <b-card no-body >
      <b-tabs pills card vertical>
        <b-tab title="评论" class="item">
          <div class="menu">
            收到的评论
          </div>
          <div class="find-nothing">
            <img src="//cdn2.jianshu.io/assets/web/icon_nocontent-00c423de394b9184d467f2f2a7284b54.png">
            <p>
              这里还没有评论~
            </p>
          </div>
        </b-tab>
        <b-tab title="简信" class="item">
          <div class="menu">
            全部简信
          </div>
          <ul class="jainxin-list">
            <li>
              <b-nav-item-dropdown text="09.07 10:14" class="pull-right">
                <b-dropdown-item href="#">删除会话</b-dropdown-item>
                <b-dropdown-item href="#">加入黑名单</b-dropdown-item>
                <b-dropdown-item href="#">举报用户</b-dropdown-item>
              </b-nav-item-dropdown>
              <a class="avatar">
                <img src="//upload.jianshu.io/users/upload_avatars/3678149/b8a58e70-1126-48c9-97e2-8f21a31dfa94.png?imageMogr2/auto-orient/strip|imageView2/1/w/144/h/144/format/webp">
              </a>
              <a class="name">简宝玉</a>
              <a class="wrap"><p>欢迎加入丰富多彩的原创内容社区—简书。新手有关简书的任何疑问请点击链接查看 http://www.jianshu.com/p/27de765cdb28 ，同时关注微信公众号简宝玉（jianshu4321)，后台回复“指南”可获取新手玩转简书社区指南详细资料礼包；简宝玉同志会专程为你答疑解惑关于简书的一切。</p></a>
            </li>
          </ul>
        </b-tab>
        <b-tab title="投稿请求" class="item">
          <div class="menu">
            全部投稿请求
          </div>
          <a class="wrap">
            <div class="push-name">全部未处理请求</div>
          </a>
        </b-tab>
        <b-tab title="喜欢和赞">
          <div class="menu">
          收到的喜欢和赞
        </div></b-tab>
        <b-tab title="关注" class="item">
          <div class="menu">
            全部关注
          </div>
        </b-tab>
        <b-tab title="赞赏和付费" class="item">
          <div class="menu">
            赞赏和付费
          </div>
        </b-tab>
        <b-tab title="其他提醒" class="item">
          <div class="menu">
            其它提醒
          </div>
        </b-tab>
      </b-tabs>
    </b-card>
  </div>
</template>

<script>
    export default {
        name: "Notifications"
    }
</script>

<style scoped>
  .push-name{
    max-width: 500px;
    font-size: 15px;
  }
  li{
    line-height: 20px;
    display: list-item;
    text-align: -webkit-match-parent;
  }
  a{
    color: #337ab7;
    text-decoration: none;
    background-color: transparent;
  }
  .wrap{
    display: block;
    padding: 20px 20px 20px 0;
  }
  .name{
    margin: 20px 20px 20px 20px;
    top: 50px;
    font-size: 15px;
  }
  .avatar{
    margin: 20px 10px 20px 20px;
    width: 48px;
    height: 48px;
  }
  ul{
    list-style: none;
    padding-left: 0;
    margin-top: 0;
    margin-bottom: 10px;
    display: block;
    list-style-type: none;
    -webkit-margin-before: 1em;
    -webkit-margin-after: 1em;
    -webkit-margin-start: 0px;
    -webkit-margin-end: 0px;
    -webkit-padding-start: 40px;
  }
  .find-nothing{
    margin-top: 150px;
    text-align: center;
  }
  .item{
    line-height: 20px;
  }
  .menu{
     margin-bottom: 20px;
    font-size: 14px;
    font-weight: 700;
  }
  .pull-right{
    margin: 20px 20px 0 0;
    font-size: 13px;
    float: right!important
  }
</style>
