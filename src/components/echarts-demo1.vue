<template>
  <div>
    <div class="echart" id="one"></div>
    <div class="echart" id="two"></div>
  </div>
</template>

<script>
import echarts from "echarts";
export default {
  name: "EchartDemo",
  mounted() {
    this.echart();
  },
  methods: {
    echart() {
      let myChart1 = echarts.init(document.getElementById("one"));
      let myChart2 = echarts.init(document.getElementById("two"));
      // 绘制图表
      myChart1.setOption({
        title: {
          text: "ECharts"
        },
        tooltip: {},
        xAxis: {
          data: ["衬衫", "羊毛衫", "雪纺衫", "裤子", "高跟鞋", "袜子"]
        },
        yAxis: {},
        series: [
          {
            name: "销量",
            type: "bar",
            data: [5, 20, 36, 10, 10, 20]
          }
        ]
      });

      myChart2.setOption({
        series: [
          {
            name: "访问来源",
            type: "pie",
            radius: "55%",
            data: [
              { value: 235, name: "视频广告" },
              { value: 274, name: "联盟广告" },
              { value: 310, name: "邮件营销" },
              { value: 335, name: "直接访问" },
              { value: 400, name: "搜索引擎" }
            ]
          }
        ]
      });
    }
  }
};
</script>
<style lang="scss" scoped>
.echart {
  width: 600px;
  height: 400px;
  border: solid 1px black;
}
</style>

