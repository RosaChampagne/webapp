<template>
  <div class="container">
    <div class="intro">Cynthia Test</div>
    
    <tui-button margin="0 0 30rpx 0" :size="34" bold @click="testClick">点击</tui-button>
    <tui-button margin="0 0 30rpx 0" :size="34" bold type="warning" open-type="contact">打开客服会话</tui-button>
    <tui-button margin="0 0 30rpx 0" :size="34" bold type="green" open-type="share">触发用户转发</tui-button>
    <tui-button margin="0 0 30rpx 0" :size="34" bold type="danger"open-type="getPhoneNumber" @getphonenumber="handleGetPhoneNumber">获取用户手机号</tui-button>
    <tui-button margin="0 0 30rpx 0" :size="34" bold type="black"open-type="getUserInfo">获取用户信息</tui-button>
    <tui-button margin="0 0 30rpx 0" :size="34" bold type="white"open-type="openSetting">打开设置权限页</tui-button>
    
    <!--toast提示-->
    <tui-toast ref="toast"></tui-toast>
  </div>
</template>

<script>
  import tuiButton from "@/components/tui-button/tui-button"
  import tuiToast from "@/components/tui-toast/tui-toast"
  
  export default {
    components:{
      tuiButton,
      tuiToast
    },
    data() {
      return {
        href: 'https://uniapp.dcloud.io/component/README?id=uniui'
      }
    },
    methods: {
      testClick () {
        let params = {
          title: '操作成功',
          content: '啦啦啦啦啦啦啦啦'
        };
        this.$refs.toast.show(params)
      }
    }
  }
</script>

<style>
  .container {
    padding: 20px;
    font-size: 14px;
    line-height: 24px;
  }
</style>
