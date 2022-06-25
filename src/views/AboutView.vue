<template>
  <div class="about-vue">
    <div class="about-">
      <el-button @click="buttonHandelClick()" >默认按钮</el-button>
      <el-button type="primary">主要按钮</el-button>
      <el-button type="success">成功按钮</el-button>
      <el-button type="info">信息按钮</el-button>
      <el-button type="warning">警告按钮</el-button>
      <el-button type="danger">危险按钮</el-button>
      <div class="c1">
        
      </div>
    </div>
  </div>
</template>

<script>
// import './AboutView.scss'
// import * as black from './AboutView-black.scss'
import * as d3 from 'd3'
export default {
  data:()=>{
    return {
      showThme : false,
    }
  },
  methods:{
    buttonHandelClick() {
      this.themeUrl = this.themeUrl == this.white ? this.black: this.white
      console.log(this.themeUrl );
    }
  }
}
</script>
  
<style>

.about-vue{
  width: 100vw;
  height: 100vh;
  /* background-color: rgba(255, 255, 255, 0.547); */
}
</style>