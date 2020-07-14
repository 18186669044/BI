<template>
  <div class="RightBox">
    <div class="topLeft">
      <div>
        <span class="fl">武汉：</span>
        <span class="fr">
          <el-progress
            :percentage="percentageObj.percentage1"
            :strokeWidth="12"
            :color="customColors"
          ></el-progress>
        </span>
      </div>
      <div>
        <span class="fl">荆州：</span>
        <span class="fr">
          <el-progress
            :percentage="percentageObj.percentage2"
            :strokeWidth="12"
            :color="customColors"
          ></el-progress>
        </span>
      </div>
      <div>
        <span class="fl">黄石：</span>
        <span class="fr">
          <el-progress
            :percentage="percentageObj.percentage3"
            :strokeWidth="12"
            :color="customColors"
          ></el-progress>
        </span>
      </div>
      <div>
        <span class="fl">随州：</span>
        <span class="fr">
          <el-progress
            :percentage="percentageObj.percentage4"
            :strokeWidth="12"
            :color="customColors"
          ></el-progress>
        </span>
      </div>
      <div>
        <span class="fl">荆门：</span>
        <span class="fr">
          <el-progress
            :percentage="percentageObj.percentage5"
            :strokeWidth="12"
            :color="customColors"
          ></el-progress>
        </span>
      </div>
    </div>
    <div class="topRight">
      <div v-if="$store.state.show" id="l-echart5-1" style="width:100%;height:100%"></div>
    </div>
    <div class="cententBox">
      <div v-if="$store.state.show" id="l-echart7-1" style="width:100%;height:100%"></div>
    </div>
    <div class="bottomLeft">
      <div v-if="$store.state.show" id="l-echart8-1" style="width:100%;height:100%"></div>
    </div>
    <div class="bottomRight">
      <div v-if="$store.state.show" id="l-echart9-1" style="width:100%;height:100%"></div>
    </div>
  </div>
</template>
<script>
import Echarts from "echarts";
import "./tools/echart-auto-tooltip";
export default {
  data() {
    return {
      customColors: [
        { color: "#f56c6c", percentage: 80 },
        { color: "#e6a23c", percentage: 100 },
        { color: "#5cb87a", percentage: 60 },
        { color: "#1989fa", percentage: 40 },
        { color: "#6f7ad3", percentage: 20 }
      ],
      percentageObj: {
        percentage1: 100,
        percentage2: 80,
        percentage3: 60,
        percentage4: 40,
        percentage5: 20
      },
      caseLeftData: [
        {
          count: 963,
          time: "2020-06-29 01"
        },
        {
          count: 921,
          time: "2020-06-29 01"
        },
        {
          count: 416,
          time: "2020-06-29 02"
        },
        {
          count: 409,
          time: "2020-06-29 03"
        },
        {
          count: 201,
          time: "2020-06-29 04"
        },
        {
          count: 760,
          time: "2020-06-29 05"
        },
        {
          count: 990,
          time: "2020-06-29 06"
        },
        {
          count: 518,
          time: "2020-06-29 07"
        },
        {
          count: 143,
          time: "2020-06-29 08"
        },
        {
          count: 205,
          time: "2020-06-29 09"
        },
        {
          count: 686,
          time: "2020-06-29 10"
        },
        {
          count: 668,
          time: "2020-06-29 11"
        },
        {
          count: 171,
          time: "2020-06-29 12"
        },
        {
          count: 713,
          time: "2020-06-29 13"
        },
        {
          count: 848,
          time: "2020-06-29 14"
        },
        {
          count: 570,
          time: "2020-06-29 15"
        },
        {
          count: 421,
          time: "2020-06-29 16"
        },
        {
          count: 691,
          time: "2020-06-29 17"
        },
        {
          count: 744,
          time: "2020-06-29 18"
        },
        {
          count: 838,
          time: "2020-06-29 19"
        },
        {
          count: 619,
          time: "2020-06-29 20"
        },
        {
          count: 416,
          time: "2020-06-29 21"
        },
        {
          count: 831,
          time: "2020-06-29 22"
        }
      ],
      CaserightList: [
        {
          count: 28,
          time: "2020-06-29 01"
        },
        {
          count: 274,
          time: "2020-06-29 01"
        },
        {
          count: 136,
          time: "2020-06-29 02"
        },
        {
          count: 646,
          time: "2020-06-29 03"
        },
        {
          count: 24,
          time: "2020-06-29 04"
        },
        {
          count: 957,
          time: "2020-06-29 05"
        },
        {
          count: 20,
          time: "2020-06-29 06"
        },
        {
          count: 991,
          time: "2020-06-29 07"
        },
        {
          count: 613,
          time: "2020-06-29 08"
        },
        {
          count: 494,
          time: "2020-06-29 09"
        },
        {
          count: 702,
          time: "2020-06-29 10"
        },
        {
          count: 137,
          time: "2020-06-29 11"
        },
        {
          count: 357,
          time: "2020-06-29 12"
        },
        {
          count: 970,
          time: "2020-06-29 13"
        },
        {
          count: 215,
          time: "2020-06-29 14"
        },
        {
          count: 180,
          time: "2020-06-29 15"
        },
        {
          count: 60,
          time: "2020-06-29 16"
        },
        {
          count: 127,
          time: "2020-06-29 17"
        },
        {
          count: 320,
          time: "2020-06-29 18"
        },
        {
          count: 41,
          time: "2020-06-29 19"
        },
        {
          count: 842,
          time: "2020-06-29 20"
        },
        {
          count: 810,
          time: "2020-06-29 21"
        },
        {
          count: 347,
          time: "2020-06-29 22"
        }
      ],
      dataList1: [
        { value: 335, name: "直接访问" },
        { value: 310, name: "邮件营销" },
        { value: 234, name: "联盟广告" }
      ],
      dataList2: [387, 932, 400, 934, 380, 1330, 400]
    };
  },
  watch: {
    "$store.state.topL": function(newVal) {
      this.percentageObj = newVal;
    },
    "$store.state.topR": function(newVal) {
      this.caseLeftData = newVal;
      this.CaseleftEcharts();
    },
    "$store.state.center": function(newVal) {
      this.CaserightList = newVal;
      this.CaserightEcharts();
    },
    "$store.state.bottomL": function(newVal) {
      this.dataList1 = newVal;
      this.CasebottomEcharts();
    },
    "$store.state.bottomR": function(newVal) {
      this.dataList2 = newVal;
      this.CaseBottomRight();
    },
    "$store.state.show": function(newVal) {
    //   console.log(newVal, "newVal");
    }
  },
  mounted() {
    this.CaseleftEcharts();
    this.CaserightEcharts();
    this.CasebottomEcharts();
    this.CaseBottomRight();
  },
  methods: {
    format(percentage) {
      return percentage === 100 ? "满" : `${percentage}%`;
    },
    CaseleftEcharts() {
      this.$nextTick(function() {
        var echartleftPieCase = Echarts.init(
          document.getElementById("l-echart5-1")
        );
        const colorList = ["#0fd7b0", "#279cff", "#ffcd06", "#fe6541"];
        //数据
        let caseList = this.caseLeftData;
        let countList = [];
        let timeList = [];
        caseList.forEach(val => {
          countList.push(val.count);
          timeList.push(val.time);
        });
        let option = {
          tooltip: {
            trigger: "axis",
            axisPointer: {
              type: "cross",
              label: {
                backgroundColor: "#6a7985"
              }
            }
          },

          color: ["#0080ff", "#4cd5ce"],
          // toolbox: {
          //   feature: {
          // saveAsImage: {}
          //   }
          // },
          grid: {
            left: 50,
            right: 50,
            top: 25,
            bottom: 50
          },
          xAxis: [
            {
              type: "category",
              boundaryGap: false,
              data: timeList,
              axisTick: {
                show: false //隐藏x坐标轴刻度
              },
              //x轴颜色
              axisLine: {
                show: true,
                lineStyle: {
                  color: "#0575ab" //x轴下线
                }
              },
              axisLabel: {
                interval: 0
              },
              //x轴字体样式
              axisLabel: {
                show: true,
                textStyle: {
                  color: "#00c3f3",
                  fontSize: "12"
                },
                formatter: function(params) {
                  var newParamsName = ""; // 最终拼接成的字符串
                  var paramsNameNumber = params.length; // 实际标签的个数
                  var provideNumber = 7; // 每行能显示的字的个数
                  var rowNumber = Math.ceil(paramsNameNumber / provideNumber); // 换行的话，需要显示几行，向上取整
                  // 条件等同于rowNumber>1
                  if (paramsNameNumber > provideNumber) {
                    /** 循环每一行,p表示行 */
                    for (var p = 0; p < rowNumber; p++) {
                      var tempStr = ""; // 表示每一次截取的字符串
                      var start = p * provideNumber; // 开始截取的位置
                      var end = start + provideNumber; // 结束截取的位置
                      // 此处特殊处理最后一行的索引值
                      if (p == rowNumber - 1) {
                        // 最后一次不换行
                        tempStr = params.substring(start, paramsNameNumber);
                      } else {
                        // 每一次拼接字符串并换行
                        tempStr = params.substring(start, end) + "\n";
                      }
                      newParamsName += tempStr; // 最终拼成的字符串
                    }
                  } else {
                    // 将旧标签的值赋给新标签
                    newParamsName = params;
                  }
                  //将最终的字符串返回
                  return newParamsName;
                }
              }
            }
          ],
          yAxis: [
            {
              type: "value",
              axisLabel: {
                // formatter: '{value} ml'
                show: true,
                textStyle: {
                  color: "#00b9e8",
                  fontSize: "12"
                }
              }
            }
          ],
          series: [
            {
              name: " ",
              type: "line",
              stack: "总量",
              itemStyle: {
                normal: {
                  //颜色渐变函数 前四个参数分别表示四个位置依次为左、下、右、上
                  color: Echarts.graphic.LinearGradient(0, 0, 0, 1, [
                    {
                      offset: 0,
                      color: "#d7f4f8" // 0% 处的颜色
                    },
                    {
                      offset: 0.5,
                      color: "#eefcfd" // 100% 处的颜色
                    },
                    {
                      offset: 1,
                      color: "#fff" // 100% 处的颜色
                    }
                  ]), //背景渐变色
                  lineStyle: {
                    // 系列级个性化折线样式
                    width: 3,
                    type: "solid",
                    color: "#4fd6d2"
                  }
                },
                emphasis: {
                  color: "#4fd6d2",
                  lineStyle: {
                    // 系列级个性化折线样式
                    width: 2,
                    type: "dotted",
                    color: "#4fd6d2" //折线的颜色
                  }
                }
              }, //线条样式
              smooth: true,
              symbolSize: 1,
              hoverAnimation: false,
              areaStyle: { normal: {} },
              data: countList
            }
          ]
        };
        echartleftPieCase.setOption(option);
        tools.loopShowTooltip(
          echartleftPieCase,
          option,
          { loopSeries: true },
          3000
        );
      });
    },
    CaserightEcharts() {
      this.$nextTick(function() {
        var echartrightPieCase = Echarts.init(
          document.getElementById("l-echart7-1")
        );
        let datatList = this.CaserightList;
        let timeList = [];
        let countList = [];
        datatList.forEach(val => {
          timeList.push(val.time);
          countList.push(val.count);
        });
        let option = {
          grid: {
            left: 50,
            right: 50,
            top: 25,
            bottom: 50
          },
          xAxis: [
            {
              type: "category",
              axisTick: {
                show: false //隐藏x坐标轴刻度
              },
              //x轴颜色
              axisLine: {
                show: true,
                lineStyle: {
                  color: "#0575ab" //x轴下线
                }
              },
              axisLabel: {
                interval: 0
              },
              //x轴字体样式
              axisLabel: {
                show: true,
                textStyle: {
                  color: "#00c3f3",
                  fontSize: "12"
                },
                formatter: function(params) {
                  var newParamsName = ""; // 最终拼接成的字符串
                  var paramsNameNumber = params.length; // 实际标签的个数
                  var provideNumber = 7; // 每行能显示的字的个数
                  var rowNumber = Math.ceil(paramsNameNumber / provideNumber); // 换行的话，需要显示几行，向上取整
                  // 条件等同于rowNumber>1
                  if (paramsNameNumber > provideNumber) {
                    /** 循环每一行,p表示行 */
                    for (var p = 0; p < rowNumber; p++) {
                      var tempStr = ""; // 表示每一次截取的字符串
                      var start = p * provideNumber; // 开始截取的位置
                      var end = start + provideNumber; // 结束截取的位置
                      // 此处特殊处理最后一行的索引值
                      if (p == rowNumber - 1) {
                        // 最后一次不换行
                        tempStr = params.substring(start, paramsNameNumber);
                      } else {
                        // 每一次拼接字符串并换行
                        tempStr = params.substring(start, end) + "\n";
                      }
                      newParamsName += tempStr; // 最终拼成的字符串
                    }
                  } else {
                    // 将旧标签的值赋给新标签
                    newParamsName = params;
                  }
                  //将最终的字符串返回
                  return newParamsName;
                }
              },
              data: timeList,
              axisPointer: {
                type: "shadow"
              }
            }
          ],
          yAxis: {
            type: "value",
            name: " ",
            axisLine: {
              show: false, //隐藏y坐标轴
              lineStyle: {
                color: "#00b9e8" //左侧y轴颜色
              }
            },
            splitLine: {},
            //y轴字体样式
            axisLabel: {
              // formatter: '{value} ml'
              show: true,
              textStyle: {
                color: "#00b9e8",
                fontSize: "12"
              }
            }
          },
          tooltip: {
            trigger: "axis",
            axisPointer: {
              // 坐标轴指示器，坐标轴触发有效
              type: "shadow" // 默认为直线，可选为：'line' | 'shadow'
            }
            // formatter: "{a} {b} : {c}"
          },
          series: [
            {
              name: " ",
              type: "bar",
              barWidth: "43%",
              z: 9,
              itemStyle: {
                normal: {
                  color: "#0fd7b0"
                }
              },
              data: countList
            }
          ]
        };
        echartrightPieCase.setOption(option);
        tools.loopShowTooltip(
          echartrightPieCase,
          option,
          { loopSeries: true },
          2000
        );
      });
    },
    CasebottomEcharts() {
      this.$nextTick(function() {
        var echartBottomPieCase = Echarts.init(
          document.getElementById("l-echart8-1")
        );
        let dataList = this.dataList1;
        const colorList = [
          "#0fd7b0",
          "#7dff23",
          "#bb8322",
          "#e4ff00",
          "#bb8322"
        ];
        let option = {
          tooltip: {
            trigger: "item",
            formatter: "{a} <br/>{b} : {c} ({d}%)"
          },
          legend: {
            orient: "vertical",
            right: "right",
            top: "30%",
            textStyle: {
              color: "#fff"
            },
            data: ["直接访问", "邮件营销", "联盟广告"]
          },
          color: colorList,
          series: [
            {
              name: "访问来源",
              type: "pie",
              radius: "55%",
              center: ["50%", "55%"],
              data: dataList,
              emphasis: {
                itemStyle: {
                  shadowBlur: 10,
                  shadowOffsetX: 0,
                  shadowColor: "rgba(0, 0, 0, 0.5)"
                }
              }
            }
          ]
        };
        echartBottomPieCase.setOption(option);
        tools.loopShowTooltip(
          echartBottomPieCase,
          option,
          { loopSeries: true },
          2000
        );
      });
    },
    CaseBottomRight() {
      this.$nextTick(function() {
        var echartBottomPieCase = Echarts.init(
          document.getElementById("l-echart9-1")
        );
        let dataList = this.dataList2;
        let option = {
          grid: {
            left: 30,
            right: 50,
            top: 10,
            bottom: 20
          },
          tooltip: {
            trigger: "axis",
            axisPointer: {
              type: "cross",
              label: {
                backgroundColor: "#6a7985"
              }
            }
          },
          xAxis: {
            type: "category",
            axisTick: {
              show: false //隐藏x坐标轴刻度
            },
            //x轴颜色
            axisLine: {
              show: true,
              lineStyle: {
                color: "#0575ab" //x轴下线
              }
            },
            axisLabel: {
              interval: 0
            },
            //x轴字体样式
            axisLabel: {
              show: true,
              textStyle: {
                color: "#00c3f3",
                fontSize: "12"
              },
              formatter: function(params) {
                var newParamsName = ""; // 最终拼接成的字符串
                var paramsNameNumber = params.length; // 实际标签的个数
                var provideNumber = 3; // 每行能显示的字的个数
                var rowNumber = Math.ceil(paramsNameNumber / provideNumber); // 换行的话，需要显示几行，向上取整
                // 条件等同于rowNumber>1
                if (paramsNameNumber > provideNumber) {
                  /** 循环每一行,p表示行 */
                  for (var p = 0; p < rowNumber; p++) {
                    var tempStr = ""; // 表示每一次截取的字符串
                    var start = p * provideNumber; // 开始截取的位置
                    var end = start + provideNumber; // 结束截取的位置
                    // 此处特殊处理最后一行的索引值
                    if (p == rowNumber - 1) {
                      // 最后一次不换行
                      tempStr = params.substring(start, paramsNameNumber);
                    } else {
                      // 每一次拼接字符串并换行
                      tempStr = params.substring(start, end) + "\n";
                    }
                    newParamsName += tempStr; // 最终拼成的字符串
                  }
                } else {
                  // 将旧标签的值赋给新标签
                  newParamsName = params;
                }
                //将最终的字符串返回
                return newParamsName;
              }
            },
            data: ["Mon", "Tue", "Wed", "Thu", "Fri", "Sat", "Sun"]
          },
          yAxis: {
            type: "value",
            axisLine: {
              show: false, //隐藏y坐标轴
              lineStyle: {
                color: "#00b9e8" //左侧y轴颜色
              }
            },
            splitLine: {},
            //y轴字体样式
            axisLabel: {
              // formatter: '{value} ml'
              show: true,
              textStyle: {
                color: "#00b9e8",
                fontSize: "12"
              }
            }
          },
          series: [
            {
              data: dataList,
              type: "line",
              smooth: true
            }
          ]
        };
        echartBottomPieCase.setOption(option);
        tools.loopShowTooltip(
          echartBottomPieCase,
          option,
          { loopSeries: true },
          2000
        );
      });
    }
  }
};
</script>
<style lang="less" scoped>
.RightBox {
  width: 100%;
  height: 100vh;
  overflow: hidden;
  color: #fff;
  .topLeft {
    width: 45%;
    height: 33.3vh;
    float: left;
    padding: 20px;
    div {
      width: 100%;
      height: 20%;
    }
    .fl {
      float: left;
      width: 10%;
    }
    .fr {
      float: right;
      width: 90%;
    }
  }
  .topRight {
    width: 55%;
    height: 33.3vh;
    float: left;
    padding: 20px;
  }
  .cententBox {
    width: 100%;
    height: 33.3vh;
    float: left;
    padding: 20px;
  }
  .bottomLeft {
    width: 45%;
    height: 33.3vh;
    float: left;
    padding: 20px;
  }
  .bottomRight {
    width: 55%;
    height: 33.3vh;
    float: left;
    padding: 20px;
  }
}

/deep/.el-progress__text {
  display: none;
}
</style>