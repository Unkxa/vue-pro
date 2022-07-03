<template>
  <div class="about-vue">
    <div class="about-">
      <el-button @click="buttonHandelClick()" >默认按钮</el-button>
      <el-button type="primary">主要按钮</el-button>
      <el-button type="success">成功按钮</el-button>
      <el-button type="info">信息按钮</el-button>
      <el-button type="warning">警告按钮</el-button>
      <el-button type="danger">危险按钮</el-button>

        <div style="font: 10px sans-serif; text-align: right; color: white;">
          <div style="background: steelblue; padding: 3px; margin: 1px; width: 40px;">4</div>
          <div style="background: steelblue; padding: 3px; margin: 1px; width: 80px;">8</div>
          <div style="background: steelblue; padding: 3px; margin: 1px; width: 150px;">15</div>
          <div style="background: steelblue; padding: 3px; margin: 1px; width: 160px;">16</div>
          <div style="background: steelblue; padding: 3px; margin: 1px; width: 230px;">23</div>
          <div style="background: steelblue; padding: 3px; margin: 1px; width: 420px;">42</div>
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
    // buttonHandelClick() {
    //   this.themeUrl = this.themeUrl == this.white ? this.black: this.white
    //   console.log(this.themeUrl );
    // }
    d3Create(){
      debugger
      const div = d3.create("div")
          .style("font", "10px sans-serif")
          .style("text-align", "right")
          .style("color", "white");
      console.log(div);
      div.selectAll("div")
        .data(data)
        .join("div")
          .style("background", "steelblue")
          .style("padding", "3px")
          .style("margin", "1px")
          .style("width", d => `${d * 10}px`)
          .text(d => d);

      return div.node();
    },
    mounted() {
      console.log('触发');
      let res = this.d3Create
      console.log(res);
    },
    created() {
      console.log('触发1')
    },
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