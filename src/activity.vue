<template>
<scroller show-scrollbar="false">
  <div class="title" :style="paddingTop">
    <text style="line-height:80px; font-size: 30px;">天津市</text>
    <wxc-icon name="more_unfold" size="small" style="margin-top:16px;"></wxc-icon>
    <div style="background-color: #f0f0f0;width:410px;height:56px;margin-left:20px;margin-top:8px;flex-direction: row;">
      <image src="https://github.com/killopept/image/blob/master/image/search.png?raw=true" style="width:40px;height:40px;margin-top:10px;margin-left:20px;"></image>
      <text style="color:#b3b3b3;font-size:26px;line-height:60px;margin-left:20px">请输入搜索内容</text>
    </div>
    <image style="width:54px;height:54px;margin-left:15px;margin-top:10px" src="https://github.com/killopept/image/blob/master/tagbar/%E6%89%AB%E4%B8%80%E6%89%AB%20(1).png?raw=true"></image>
    <image style="width:54px;height:54px;margin-left:15px;margin-top:10px" src="https://github.com/killopept/image/blob/master/tagbar/%E6%B6%88%E6%81%AF%20(2).png?raw=true"></image>
  </div>
  <div class="activity">
    <div style="margin-bottom:20px;">
      <image style="width:700;height:254px" src="https://github.com/killopept/image/blob/master/banner/activety1.png?raw=true"></image>
    </div>
    <div style="margin-bottom:20px;">
      <image style="width:700;height:254px" src="https://github.com/killopept/image/blob/master/banner/activety2.png?raw=true"></image>
    </div>
    <div style="margin-bottom:20px;">
      <image style="width:700;height:254px" src="https://github.com/killopept/image/blob/master/banner/activety3.png?raw=true"></image>
    </div>
    <div style="margin-bottom:20px;">
      <image style="width:700;height:254px" src="https://github.com/killopept/image/blob/master/banner/activety4.png?raw=true"></image>
    </div>
    <div style="margin-bottom:20px;">
      <image style="width:700;height:254px" src="https://github.com/killopept/image/blob/master/banner/activety5.png?raw=true"></image>
    </div>
  </div>
</scroller>
</template>

<style>
  .activity{
    padding:10px 25px;
    padding-top: 20px;
  }
  .title{
    height: 100px;
    background-color:#fff;
    padding: 14px 30px;
    flex-direction: row;
  }
</style>

<script>
  import {WxcIcon} from 'weex-ui'
  export default {
    data () {
      return {
        paddingTop: {},
        object: WXEnvironment
      }
    },
    components: {WxcIcon},
    mounted () {
      this.paddingTop = {}
      if (this.object.platform !== 'iOS') {
        return
      }
      if (this.object.deviceModel === 'iPhone10,3') {
        this.paddingTop = {paddingTop : '78px', height: 100 + 64 + 'px'}
      } else {
        this.paddingTop = {paddingTop : '34px', height: 100 + 20 + 'px'}
      }
    }
  }
</script>