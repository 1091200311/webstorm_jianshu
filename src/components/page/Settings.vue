<template>
  <b-card no-body>
    <b-tabs pills card vertical>
      <b-tab title="基础设置">
        <!--<table>-->
          <!--<tr style="display: table-row;vertical-align: inherit">-->
            <!--<td>提醒邮件通知</td>-->
            <!--<td>-->
              <!--<div class="col-xs-8">-->
                <!--<input type="radio" value="instantly">-->
                <!--<span>所有动态</span>-->
              <!--</div>-->
              <!--<div class="col-xs-8">-->
                <!--<input type="radio" value="instantly">-->
                <!--<span>所有动态</span>-->
              <!--</div>-->
            <!--</td>-->
          <!--</tr>-->
        <!--</table>-->
        <input type="submit" class="btn-success" value="保存">
      </b-tab>
      <b-tab title="个人资料">
        <input type="submit" class="btn-success" value="保存">
      </b-tab>
      <b-tab title="微博认证">
      </b-tab>
      <b-tab title="黑名单">
        <div class="title">你可以在用户主页将用户加入你的黑名单。在你黑名单中的用户无法在你文章下评论，无法在其它评论中提到你，无法给你发送简信，自动从你的粉丝列表移除且无法再关注你。</div>
      </b-tab>
      <b-tab title="赞赏设置">
        <input type="submit" class="btn-success" value="保存">
      </b-tab>
      <b-tab title="账号设置">
      </b-tab>
    </b-tabs>
  </b-card>
</template>

<script>
    export default {
        name: "Settings"
    }
</script>

<style scoped>
.col-xs-8{
  width: 33.33%;
}
.title{
  font-size: 12px;
  color: #969696;
}
</style>
