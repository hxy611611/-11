<template>
  <div id="app">
    
    <div class="header">
      <div class="header-up">
        <img height="100%" src="./assets/1.jpg" alt="">
        <div class="search-box">
          <div class="serch-box-in">
            <input style="height:15px; width:120px;" type="text">
            <button style="height:25px;">查询</button>
          </div>
        </div>
      </div>
      <div class="header-down">
        <div class="nav-item">网站首页</div>
        <div class="nav-item">品牌空间</div>
        <div class="nav-item">全线车系</div>
        <div class="nav-item">企业信息</div>
        <div class="nav-item">预约试驾</div>
        <div class="nav-item">经销商查询</div>
        <div class="nav-item">专家答疑</div>
        <div class="nav-item">红旗服务</div>
      </div>
    </div>


    <div class="center">
      <div class="center-navi">
        <div class="center-navi-title">车型分类</div>
        <div class="center-navi-item" @click="showCar('p')">红旗H5</div>
        <div class="center-navi-item" @click="showCar('t')">红旗H6</div>
        <div class="center-navi-item" @click="showCar('e')">红旗L5</div>


      </div>
      <div class="center-bigimg" >
        <!-- <img src="./assets/t1.png" class="big-img" alt=""> -->
        <!-- <img src="require('./assets/t1.png')" alt=""> -->
        <img :src="require('@/assets/' + currentCar +changeBig+'.jpg')" class="big-img" alt="">
      </div>
      
      <div class="center-smalling" >
        <img @click="showBig(1)" class="small-img" :src="require('./assets/' +currentCar + '1.jpg')" alt="" >
        <img @click="showBig(2)" class="small-img" :src="require('./assets/' +currentCar + '2.jpg')" alt="">
        <img @click="showBig(3)" class="small-img" :src="require('./assets/' +currentCar + '3.jpg')" alt="">
        <img @click="showBig(4)" class="small-img" :src="require('./assets/' +currentCar + '4.jpg')" alt="">
      </div>
    </div>


    <div class="footer">
      <span><a href="#">网站地图</a> &nbsp;&nbsp;&nbsp;&nbsp;
        <a href="#">购车计算器</a>&nbsp;&nbsp;&nbsp;&nbsp;
        <a href="#">免责声明</a> &nbsp;&nbsp;&nbsp;&nbsp;
        <a href="#">联系红旗</a></span>
      <span>版权所有******.hxy专有</span>
    </div>
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'

export default {
 data(){
  return{
    currentCar:'p',
    changeBig:'1'
  }
 },
 methods:{
  // showH5() {
  //   this.currentCar = 'H5'
  // }
  showCar(x) {
    this.currentCar = x;
  },
showBig(x) {
  this.changeBig = x;
}
 }



}
</script>

<style>
a{
  color: white;
  text-decoration: none;
  font-weight: bold;
}
#app {
 width: 100%;
 height: 100%;
 left: 0px;
 top: 0px;
/* background-color: pink;*/
 position: absolute;
}
/*头部*/
.header {
  width: 100%;
  height: 25%;
  /*background-color: yellow;*/
 /* border-bottom: 2px solid red;*/
 
}

.header-up {
  width: 100%;
  height: 50%;
  background-color:white;
  display: flex;
  justify-content: space-between;
}
.search-box {
  width: 20%;
  height: 100%;
  background-color: red;
  display: flex;
  justify-content: center;
  align-items: center;
}

.serch-box-in{
  width:90%;
  height: 70%;
  background-color: brown;
  display: flex;
  align-items: center;
  justify-content: space-around;
}


/*中间部分*/
.header-down{
  width: 100%;
  height: 20%;
  background-color: white;
  display: flex;
  align-items: flex-end;
  /*margin-bottom: -100px;*/
  border-bottom: 2px solid red;
  font-weight: bold;
  cursor: pointer;

}
.nav-item{
  width: 10%;
  height: 100%;
  /*background-color: chartreuse;*/
  margin-left: 10px;
  display: flex;
  justify-content: center;
  align-items: center;
  color: red;
  font-weight: font;
  
}
.center {
  width: 100%;
  height: 77%;
  background-color: white;
  display: flex;
  align-items: center;
}
.center-navi{
  height: 90%;
  width: 15%;
  /*background-color: aqua;*/
}
.center-navi-title{
  height: 8%;
  width: 80%;
  /*background-color:white;*/
  border-bottom-style: solid;
  border-bottom-color: red;
  display: flex;
  align-items: flex-end;
  padding-left: 20px;
  font-size: 20px;
  margin-top: -40px;
  /*padding-right: 130px;*/
  color: red;
}
.center-navi-item{
  width: 80%;
  height: 8%;
  border-bottom-style: dotted;
  border-bottom-color: red;
  border-bottom-width: 2px;
  padding-left: 20px;
  display: flex;
  align-items: flex-end;
  color: red;
  font-weight: bold;
  cursor: pointer;/*放上去是手指*/
}
.center-bigimg{
  height: 90%;
  width: 65%;
  /*background-color: rgb(158, 103, 32);*/
  display: flex;
  flex-direction: column;

}
.big-img{
  width: 90%;
  height: 90%;
}
.small-img{
  width: 80%;
  height: 23%;
}
.center-smalling{
  height: 90%;
  width: 20%;
  /*background-color: aquamarine;*/
}


/*底部*/
.footer {
  width: 100%;
  height: 8%;
  background-color: red;
  display: flex;
  flex-direction: column;
  color: white;
  align-items: center;
  justify-content: center;
  font-weight: bold;
}
</style>
