<template>
  <div>
    <h1 v-if="into">
      <img src="/img/app_download_parent_img_new.png" alt="">
      <p>报的好，学得对</p> 
    </h1>
    <div v-else id="room">
      <div class="top">
        <h3 class="groupChat">群聊大厅</h3>
        <h3 class="singleChat">单聊</h3>
      </div>
      <div class="msgContent">
        <p class="currentLine">当前在线<span>12</span></p>
      </div>
      <div class="bottom_send">
        <input class="content" type="text">
        <input id="send" type="button" value="发送"/>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data () {
    return {
      into: true
    }
  },
  mounted () {
    setTimeout(() => {
      this.into = false
    }, 3000)
  },
  head: {
    bodyAttrs: {
      class: 'fff'
    }
  }
}
</script>
<style lang="sass" scoped>
@import '~static/common/style.sass'
@-webkit-keyframes fadeIn
  0%
    opacity: 1
  20%
    opacity: 0.9
  30%
    opacity: 0.8
  40%
    opacity: 0.7
  50%
    opacity: 0.6
  60%
    opacity: 0.5
  70%
    opacity: 0.4
  80%
    opacity: 0.3
  100%
    opacity: 0
h1
  position: absolute
  top: 50%
  transform: translateY(-50%)
  width: 100%
  text-align: center
  margin-top: -50px
  animation: fadeIn 0.8s 3s forwards
  p
    color: $theme_color
    margin-top: 20px
    font-weight: normal
#room
  .top
    height: 48px
    width: 100%
    background: $theme_fu_org
    h3
      float: left
      width: 50%
      height: 48px
      color: #fff
      text-align: center
      line-height: 48px
      font-size: 16px
    .singleChat
      border-left: 1px solid #fff
  .msgContent
    .currentLine
      text-align: center
      margin-top: 10px
      color: $theme_gray999
  .bottom_send
    height: 33px
    background: $theme_fu_red
    width: 100%
    position: fixed
    bottom: 0
    left: 0
    .content
      float: left
      height: 29px
      width: 80%
      margin-top: 2px
      margin-left: 2px
      padding-left: 6px
    #send
      color: #fff
      width: 19%
      height: 33px
      line-height: 34px
      background: $theme_fu_red
</style>

