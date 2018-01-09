<template>
  <div>
    <scroller lock-y :scrollbar-x=false>
      <div class="box1">
        <div class="box1-item" v-for="i in nav"><span>{{' ' + i + ' '}}</span></div>
      </div>
    </scroller>
    <div class="clearfix">
      <img class="banner" src="../../common/img/banner.jpg" alt="">
    </div>
    <div class="filter_out dis-fl">
      <div class="filter1"><span class="text tran-center">仅显示</br>可报价</span></div>
      <div class="filter2">
        <group>
          <selector placeholder="请选择省份" v-model="kind" :options="pur_kind"></selector>
        </group>
      </div>
      <div class="filter2">
          <selector class="select" placeholder="采购类型" v-model="kind" name="district" :options="pur_kind" @on-change="onChange"></selector>
      </div>
      <button class="purchase">发采购</button>
    </div>
    <div>
      <div class="list_out">
        <div class="item dis-fl">
          <div class="flex-1 left">
            <div class="name">求购钢材</div>
            <div class="adress">
              <span class="col-a3 pull-left">100KG</span>
              <span class="col-a3 pull-right">辽宁</span>
            </div>
          </div>
          <div class="right">
            <div class="time">2天截止</div>
            <div>
              <button class="quote">报价</button>
            </div>
          </div>
        </div>
        <div class="item dis-fl">
          <div class="flex-1 left">
            <div class="name">求购钢材</div>
            <div class="adress">
              <span class="col-a3 pull-left">100KG</span>
              <span class="col-a3 pull-right">辽宁</span>
            </div>
          </div>
          <div class="right">
            <div class="time">2天截止</div>
            <div>
              <button class="quote done">已报价</button>
            </div>
          </div>
        </div>
        <div class="item dis-fl">
          <div class="flex-1 left">
            <div class="name">求购钢材</div>
            <div class="adress">
              <span class="col-a3 pull-left">100千克</span>
              <span class="col-a3 pull-right">辽宁</span>
            </div>
          </div>
          <div class="right">
            <div>
              <button class="quote end">已截止</button>
            </div>
          </div>
        </div>
        <div class="item dis-fl">
          <div class="flex-1 left">
            <div class="name">求购钢材</div>
            <div class="adress">
              <span class="col-a3 pull-left">100KG</span>
              <span class="col-a3 pull-right">辽宁</span>
            </div>
          </div>
          <div class="right">
            <div class="time">2天截止</div>
            <div>
              <button class="quote">报价</button>
            </div>
          </div>
        </div>
        <div class="item dis-fl">
          <div class="flex-1 left">
            <div class="name">求购钢材</div>
            <div class="adress">
              <span class="col-a3 pull-left">100KG</span>
              <span class="col-a3 pull-right">辽宁</span>
            </div>
          </div>
          <div class="right">
            <div class="time">2天截止</div>
            <div>
              <button class="quote">报价</button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { Scroller, Selector, XButton, Group } from 'vux'

export default {
  components: {
    Scroller,
    Selector,
    XButton,
    Group
  },
  data () {
    return {
      nav: ['首页', '求购大厅', '新闻', '行情', '行情', '行情', '行情'],
      pur_kind: [{key: 'gd', value: '筛选类型'}, {key: 'gx', value: '类型一'}],
      kind: ''
    }
  },
  methods: {
    onChange () {

    }
  }
}
</script>
<style>
  @import '../../common/styles/comm';
  .banner {
    float: left;
    width: 100%;
  }
  .filter_out {
    align-items: center;
    justify-content: space-between;
    padding: 0.1rem 0.1rem;
  }
  .filter1 {
    position: relative;
    height: 0.48rem;
    width: 0.48rem;
    float: left;
    border-radius: 50%;
    border: 1px solid #35b26e;
    color: #35b26e;
    text-align: center;
    font-size: 0.1rem
  }
  .filter1 .text{
    width: 0.5rem
  }
  .filter2 {
    float: left;
    height: 0.4rem;
    border: 1px solid #ccc;
    border-radius: 0.16rem
  }
  .select .weui-select{
    height: 0.4rem;
    line-height: 0.4rem;
    border-radius: 10px;
  }
  .purchase{
    width: 0.76rem;
    height: 0.3rem;
    border: 1px solid #32b16c;
    color: #fff;
    font-size: 0.16rem;
    border-radius: 0.03rem;
    background: #32b16c
  }
  .list_out {
    padding-top: 0.15rem;
    background: #e8e8ed;
  }
  .item{
    align-items: center;
    padding: 0.15rem 0.1rem;
    background: #fff;
  }
  .item+.item{
    border-top: 0.02rem solid #f3f3f5
  }
  .item .name{
    width: 100%;
    font-size: 0.18rem;
    margin-bottom: 0.05rem;
  }
  .item .right{
    width: 0.68rem;
  }
  .item .time{
    text-align: center;
    font-size: 0.15rem;
    color: #ec6941;
    margin-bottom: 0.05rem;
  }
  .item .adress {
    padding-right: 0.4rem
  }
  .quote {
    width: 0.68rem;
    height: 0.26rem;
    border: 1px solid #1593ff;
    color: #1593ff;
    font-size: 0.14rem;
    border-radius: 0.04rem;
    background: #fff
  }
  .done {
    color: #fff;
    background: #1593ff
  }
  .end{
    border: 1px solid #bfbfbf;
    color: #fff;
    background:  #bfbfbf
  }
 .box1 {
  font-size: 0.12rem;
  height: 0.35rem;
  position: relative;
  width: 1300px;
}
.box1-item {
  width: 1.5rem;
  height: 0.35rem;
  background-color: #ccc;
  display:inline-block;
  margin-left: 0.15rem;
  float: left;
  text-align: center;
  line-height: 0.35rem;
}
.box1-item:first-child {
  margin-left: 0;
}
.box2-wrap {
  height: 3rem;
  overflow: hidden;
}
</style>
