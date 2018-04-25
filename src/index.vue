<template>
<scroller show-scrollbar="false">
  <div class="container">
    <div class="title" :style="paddingTop">
      <text style="line-height:80px; font-size: 30px;">天津市</text>
      <wxc-icon name="more_unfold" size="small" style="margin-top:16px;"></wxc-icon>
      <div style="background-color: #f0f0f0;width:410px;height:56px;margin-left:20px;margin-top:8px;flex-direction: row;">
        <image src="https://github.com/killopept/image/blob/master/image/search.png?raw=true" style="width:40px;height:40px;margin-top:10px;margin-left:20px;"></image>
        <text style="color:#b3b3b3;font-size:26px;line-height:60px;margin-left:20px">请输入搜索内容</text>
      </div>
      <image style="width:54px;height:54px;margin-left:15px;margin-top:10px" src="https://github.com/killopept/image/blob/master/tagbar/%E6%89%AB%E4%B8%80%E6%89%AB.png?raw=true"></image>
      <image style="width:54px;height:54px;margin-left:15px;margin-top:10px" src="https://github.com/killopept/image/blob/master/tagbar/%E6%B6%88%E6%81%AF.png?raw=true"></image>
    </div>
    <div class="main">
    <slider class="slider size" auto-play="true">
      <div v-for="(src,index) in posters" :key="index">
        <image class="size" :src="src"></image>
      </div>
      <indicator class="indicator"></indicator>
    </slider>
    <div class="titleBar">
      <div class="simplePic">
        <image src="https://github.com/killopept/image/blob/master/tagbar/titleBar1.png?raw=true" class="picture"></image>
        <div>
          <text class="picbottom">投资</text>
        </div>
      </div>
      <div class="simplePic">
        <image src="https://github.com/killopept/image/blob/master/tagbar/titleBar2.png?raw=true" class="picture"></image>
        <div>
          <text class="picbottom">基金</text>
        </div>
      </div>
      <div class="simplePic">
        <image src="https://github.com/killopept/image/blob/master/tagbar/titleBar3.png?raw=true" class="picture"></image>
        <div>
          <text class="picbottom">保险</text>
        </div>
      </div>
      <div class="simplePic">
        <image src="https://github.com/killopept/image/blob/master/tagbar/titleBar4.png?raw=true" class="picture"></image>
        <div>
          <text class="picbottom">黄金</text>
        </div>
      </div>
      <div class="simplePic">
        <image src="https://github.com/killopept/image/blob/master/tagbar/titleBar5.png?raw=true" class="picture"></image>
        <div>
          <text class="picbottom">银证交易</text>
        </div>
      </div>
      <div class="simplePic">
        <image src="https://github.com/killopept/image/blob/master/tagbar/titleBar6.png?raw=true" class="picture"></image>
        <div>
          <text class="picbottom">生活缴费</text>
        </div>
      </div>
      <div class="simplePic">
        <image src="https://github.com/killopept/image/blob/master/tagbar/titleBar7.png?raw=true" class="picture"></image>
        <div>
          <text class="picbottom">电影</text>
        </div>
      </div>
      <div class="simplePic">
        <image src="https://github.com/killopept/image/blob/master/tagbar/titleBar8.png?raw=true" class="picture"></image>
        <div>
          <text class="picbottom">旅行</text>
        </div>
      </div>
      <div class="simplePic">
        <image src="https://github.com/killopept/image/blob/master/tagbar/titleBar9.png?raw=true" class="picture"></image>
        <div>
          <text class="picbottom">手机充值</text>
        </div>
      </div>
      <div class="simplePic">
        <image src="https://github.com/killopept/image/blob/master/tagbar/titleBar10.png?raw=true" class="picture"></image>
        <div>
          <text class="picbottom">全部</text>
        </div>
      </div>
    </div>
    <!--<div @click="run">
      <text>RUN function</text>
    </div>-->
    <div class="empty"></div>
    <div class="adv">
      <image style="width:750px;height:221px" src="https://github.com/killopept/image/blob/master/banner/banner4.png?raw=true"></image>
    </div>
    <div class="empty"></div>
    <div class="gold">
      <div class="goldTitle">
        <text style="font-size:30px">基金</text>
      </div>
      <div class="goldMiddle">
        <div class="gold_left">
          <div style="flex-direction:row">
            <text style="color:red;font-size:30px">19.51</text>
            <text class="percent">%</text>
          </div>
          <text class="detail">近一年涨幅</text>
        </div>
        <div class="gold_right">
          <text style="font-size:30px">富国天瑞强势混合</text>
          <text class="detail">长期优秀强势霸榜</text>
        </div>
      </div>
      <div class="goldMiddle">
        <div class="gold_left">
          <div style="flex-direction:row">
            <text style="color:red;font-size:30px">4.796</text>
            <text class="percent">%</text>
          </div>
          <text class="detail">七日年化收益率</text>
        </div>
        <div class="gold_right">
          <text style="font-size:30px">民生加银家盈理财7天债券A</text>
          <text class="detail">到期前不可取</text>
        </div>
      </div>
    </div>
    <div class="safe">
      <div class="safeTitle">
        <text style="font-size:30px">保险</text>
      </div>
      <div class="safeMiddle">
        <div class="safeItems">
          <div>
            <text style="font-size:30px">全家保</text>
          </div>
          <div class="itemMiddle">
            <text class="number">￥77</text>
            <text class="person">/人团购</text>
          </div>
          <div>
            <text class="itemBottom">10万</text>
          </div>
        </div>
        <div class="safeItems">
          <div>
            <text style="font-size:30px">天下无疾</text>
          </div>
          <div class="itemMiddle">
            <text class="number">￥65.5</text>
            <text class="person">起保</text>
          </div>
          <div>
            <text class="itemBottom">50万</text>
          </div>
        </div>
        <div class="safeItems">
          <div>
            <text style="font-size:30px">尊享E生</text>
          </div>
          <div class="itemMiddle">
            <text class="number">￥136</text>
            <text class="person">起保</text>
          </div>
          <div>
            <text class="itemBottom">600万</text>
          </div>
        </div>
      </div>
    </div>
    <div class="money">
      <div class="moneyTitle">
        <text style="font-size: 30px">黄金</text>
      </div>
      <div class="moneyDec">
        <div>
          <div class="itemTitle">
            <text class="moneyNumber">4.500</text>
            <text class="kilo">克/100克</text>
          </div>
          <text class="year">预计年化收益克重</text>
        </div>
        <div>
          <div>
            <text style="font-size:30px;padding-top:3px;">优长金A0000004347</text>
          </div>
          <div class="buttonAll">
            <div class="buttonLeft">
              <text style="font-size:25px">1000克起</text>
            </div>
            <div class="buttonRight">
              <text style="font-size:25px">期限100天</text>
            </div>
          </div>
        </div>
        <div class="itemsRight">
          <text class="button">购买</text>
        </div>
      </div>
    </div>
    <div class="money">
      <div class="moneyTitle">
        <text style="font-size: 30px">黄金</text>
      </div>
      <div class="moneyDec">
        <div>
          <div class="itemTitle">
            <text class="moneyNumber">4.500</text>
            <text class="kilo">克/100克</text>
          </div>
          <text class="year">预计年化收益克重</text>
        </div>
        <div>
          <div>
            <text style="font-size:30px;padding-top:3px;">优长金A0000004347</text>
          </div>
          <div class="buttonAll">
            <div class="buttonLeft">
              <text style="font-size:25px">1000克起</text>
            </div>
            <div class="buttonRight">
              <text style="font-size:25px">期限100天</text>
            </div>
          </div>
        </div>
        <div class="itemsRight">
          <text class="button">购买</text>
        </div>
      </div>
    </div>
    <div class="money">
      <div class="moneyTitle">
        <text style="font-size: 30px">黄金</text>
      </div>
      <div class="moneyDec">
        <div>
          <div class="itemTitle">
            <text class="moneyNumber">4.500</text>
            <text class="kilo">克/100克</text>
          </div>
          <text class="year">预计年化收益克重</text>
        </div>
        <div>
          <div>
            <text style="font-size:30px;padding-top:3px;">优长金A0000004347</text>
          </div>
          <div class="buttonAll">
            <div class="buttonLeft">
              <text style="font-size:25px">1000克起</text>
            </div>
            <div class="buttonRight">
              <text style="font-size:25px">期限100天</text>
            </div>
          </div>
        </div>
        <div class="itemsRight">
          <text class="button">购买</text>
        </div>
      </div>
    </div>
    <div class="empty"></div>
    <div>
      <image style="width: 750px;height:228px" src="https://github.com/killopept/image/blob/master/banner/banner2.png?raw=true"></image>
    </div>
    <div class="empty"></div>
    <div class="shopping">
      <div class="shoppingTitle">
        <text style="font-size: 35px;">好享购</text>
        <text class="more">更多</text>
      </div>
      <div class="shoppingMiddle">
        <div class="shoppingItem">
          <image style="width: 141px;height:141px" src="https://github.com/killopept/image/blob/master/tagbar/titleBar21.png?raw=true"></image>
          <text style="font-size: 28px">夏日浪漫</text>
          <text style="font-size: 25px;color:#ccc">全积分零元购</text>
        </div>
        <div class="shoppingItem">
          <image style="width:141px;height:141px" src="https://github.com/killopept/image/blob/master/tagbar/titleBar22.png?raw=true"></image>
          <text style="font-size: 28px">甜蜜蛋糕</text>
          <text style="font-size: 25px;color:#ccc">满198减50元</text>
        </div>
        <div class="shoppingItem">
          <image style="width:141px;height:141px" src="https://github.com/killopept/image/blob/master/tagbar/titleBar23.png?raw=true"></image>
          <text style="font-size: 28px">生鲜全积分</text>
          <text style="font-size: 25px;color:#ccc">折上折减80元</text>
        </div>
      </div>
    </div>
    <div class="empty"></div>
      <div>
        <image style="width:750px;height:228px;" src="https://github.com/killopept/image/blob/master/banner/banner3.png?raw=true"></image>
      </div>
    <div class="empty"></div>
  </div>
  </div>
</scroller>
</template>
<script>
import {WxcIcon} from 'weex-ui'
// import Header from './header.vue'
export default {
  name: 'App',
  data () {
    return {
      posters: [
        'https://github.com/killopept/image/blob/master/banner/banner1.png?raw=true',
        'https://github.com/killopept/image/blob/master/banner/banner1.png?raw=true',
        'https://github.com/killopept/image/blob/master/banner/banner1.png?raw=true'
      ],
      paddingTop: {},
      object: WXEnvironment
    }
  },
  components: { WxcIcon },
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

<style scoped>
  .container {
    width: 750px;
  }
  .title{
    height: 100px;
    background-color:#3574c4;
    padding: 14px 30px;
    flex-direction: row;
  }
  .main {
    width:750px;
  }
  .size {
    width: 750px;
    height: 206px;
  }
  .slider {
    position: relative;
  }
  .indicator {
    width: 750px;
    position: absolute;
    left: 0;
    right: 0;
    bottom: 0;
    height: 60px;
    background-color: rgba(0, 0, 0, 0.3);
    itemColor: #DDDDDD;
    itemSelectedColor: rgb(0, 180, 255);
  }
  .titleBar {
    width: 750px;
    height: 300px;
    flex-direction: row;
    justify-content: flex-start;
    flex-wrap: wrap;
  }
  .picture {
    width: 55px;
    height: 55px;
    margin: 10px auto;
  }
  .simplePic {
    width:150px;
    height: 150px;
    align-items: center;
    justify-content: center;
  }
  .picbottom{
    font-size:25px;
    text-align:center;
  }
  .empty {
    background-color: #f7f7f7;
    width: 750px;
    height: 20px;
  }
  .gold{
    padding-left:20px;
  }
  .goldTitle{
    padding: 15px 0;
  }
  .goldMiddle {
    flex-direction: row;
    justify-content: flex-start;
    flex-wrap: nowrap;
  }
  .gold_left {
    width: 225px;
  }
  .gold_right {
    width: 425px
  }
  .percent {
    color:red;
    font-size:15px;
    height:30px;
    line-height:48px
  }
  .detail {
    font-size: 20px;
    margin:10px 0 30px 0;
  }
  .safe {
    width: 750px;
  }
  .safeTitle {
    padding: 20px 15px;
  }
  .safeMiddle {
    padding: 0 40px;
    flex-direction: row;
    justify-content: space-between;
    flex-wrap: nowrap;
  }
  .safeItems{
    align-items: center;
    justify-content: center
  }
  .number, .itemBottom {
    font-size: 35px;
    color: red;
  }
  .person {
    padding-top: 13px;
    font-size: 20px;
  }
  .itemMiddle{
    flex-direction: row;
    margin:15px 0;
  }
  .money {
    padding:0 20px;
    padding-bottom: 20px;
  }
  .moneyTitle{
    padding: 15px 0;
  }
  .moneyDec {
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
  }
  .itemTitle {
    flex-direction: row;
  }
  .moneyNumber {
    font-size: 35px;
    color: orange;
  }
  .kilo {
    font-size: 25px;
    color: orange;
    padding-top: 9px;
  }
  .year {
    font-size: 25px;
    margin-top:10px;
  }
  .buttonAll {
    flex-direction: row;
    margin-top:5px;
  }
  .buttonLeft,.buttonRight,{
    padding: 3px 10px;
    border-width: 1px;
    border-radius: 10px;
    text-align: center;
    border-style: solid;
    border-color: #f1c171;
  }
  .buttonRight {
    margin-left:5px;
  }
  .button {
    width: 100px;
    height: 40px;
    border-width: 1px;
    border-radius: 30px;
    border-color: #f1c171;
    background-color: #f1c171;
    text-align: center;
    line-height: 40px;
    font-size: 25px;
  }
  .shopping{
    widt:750px;
    padding-left: 10px;
  }
  .shoppingTitle {
    flex-direction: row;
    padding:10px;
    align-items: center;
    border-bottom-width: 1px;
    border-bottom-style:solid;
    border-bottom-color: #000;
  }
  .more {
    width: 600px;
    text-align: right;
    font-size: 25px;
  }
  .shoppingMiddle{
    flex-direction: row;
    flex-wrap: nowrap;
    justify-content: space-between;
  }
  .shoppingItem {
    width: 220px;
    padding: 10px 0;
    align-items: center;
  }
</style>
