<template>
  <div class="mapBox">
    <!-- <div id="map" style="width:100%;height:100%"></div> -->
    <div class="mapbuttom">
      <el-row>
        <el-button @click="EchartsData(1)">青山区</el-button>
        <el-button @click="EchartsData(2)" type="primary">洪山区</el-button>
        <el-button @click="EchartsData(3)" type="success">江夏区</el-button>
        <el-button @click="EchartsData(4)" disabled type="info">硚口区</el-button>
        <el-button @click="EchartsData(5)" disabled type="warning">武昌</el-button>
        <el-button @click="EchartsData(6)" disabled type="danger">汉口</el-button>
      </el-row>
    </div>
  </div>
</template>
<script>
import Echarts from "echarts";
export default {
  mounted() {
    // this.mapDataEcharts();
  },
  methods: {
    EchartsData(i) {
      this.$store.state.show = false;
      if (i == 1) {
        setTimeout(() => {
          this.$store.state.topL = {
            percentage1: 90,
            percentage2: 80,
            percentage3: 70,
            percentage4: 60,
            percentage5: 50
          };
          this.$store.state.topR = [
            {
              count: 564,
              time: "2020-06-29 01"
            },
            {
              count: 342,
              time: "2020-06-29 01"
            },
            {
              count: 416,
              time: "2020-06-29 02"
            },
            {
              count: 567,
              time: "2020-06-29 03"
            },
            {
              count: 498,
              time: "2020-06-29 04"
            },
            {
              count: 689,
              time: "2020-06-29 05"
            },
            {
              count: 990,
              time: "2020-06-29 06"
            },
            {
              count: 467,
              time: "2020-06-29 07"
            },
            {
              count: 165,
              time: "2020-06-29 08"
            },
            {
              count: 123,
              time: "2020-06-29 09"
            },
            {
              count: 432,
              time: "2020-06-29 10"
            }
          ];
          this.$store.state.center = [
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
            }
          ];
          this.$store.state.bottomL = [
            { value: 335, name: "直接访问" },
            { value: 310, name: "邮件营销" },
            { value: 234, name: "联盟广告" }
          ];
          this.$store.state.bottomR = [387, 932, 400, 934, 380, 1330, 400];
          this.$store.state.show = true;
        }, 0);
      }
      if (i == 2) {
        setTimeout(() => {
          this.$store.state.topL = {
            percentage1: 10,
            percentage2: 20,
            percentage3: 30,
            percentage4: 40,
            percentage5: 50
          };
          this.$store.state.topR = [
            {
              count: 123,
              time: "2020-06-29 01"
            },
            {
              count: 455,
              time: "2020-06-29 01"
            },
            {
              count: 232,
              time: "2020-06-29 02"
            },
            {
              count: 564,
              time: "2020-06-29 03"
            },
            {
              count: 567,
              time: "2020-06-29 04"
            },
            {
              count: 876,
              time: "2020-06-29 05"
            },
            {
              count: 987,
              time: "2020-06-29 06"
            },
            {
              count: 456,
              time: "2020-06-29 07"
            },
            {
              count: 142,
              time: "2020-06-29 08"
            },
            {
              count: 154,
              time: "2020-06-29 09"
            },
            {
              count: 653,
              time: "2020-06-29 10"
            }
          ];
          this.$store.state.center = [
            {
              count: 43,
              time: "2020-06-29 06"
            },
            {
              count: 876,
              time: "2020-06-29 07"
            },
            {
              count: 569,
              time: "2020-06-29 08"
            },
            {
              count: 489,
              time: "2020-06-29 09"
            },
            {
              count: 345,
              time: "2020-06-29 10"
            },
            {
              count: 236,
              time: "2020-06-29 11"
            },
            {
              count: 567,
              time: "2020-06-29 12"
            },
            {
              count: 982,
              time: "2020-06-29 13"
            },
            {
              count: 198,
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
              count: 346,
              time: "2020-06-29 18"
            }
          ];
          this.$store.state.bottomL = [
            { value: 456, name: "直接访问" },
            { value: 123, name: "邮件营销" },
            { value: 876, name: "联盟广告" }
          ];
          this.$store.state.bottomR = [123, 654, 400, 456, 987, 123, 1322];
          this.$store.state.show = true;
        }, 0);
      }
      if (i == 3) {
        setTimeout(() => {
          this.$store.state.topL = {
            percentage1: 40,
            percentage2: 50,
            percentage3: 60,
            percentage4: 70,
            percentage5: 80
          };
          this.$store.state.topR = [
            {
              count: 876,
              time: "2020-06-29 01"
            },
            {
              count: 464,
              time: "2020-06-29 01"
            },
            {
              count: 767,
              time: "2020-06-29 02"
            },
            {
              count: 246,
              time: "2020-06-29 03"
            },
            {
              count: 146,
              time: "2020-06-29 04"
            },
            {
              count: 588,
              time: "2020-06-29 05"
            },
            {
              count: 168,
              time: "2020-06-29 06"
            },
            {
              count: 855,
              time: "2020-06-29 07"
            },
            {
              count: 578,
              time: "2020-06-29 08"
            },
            {
              count: 136,
              time: "2020-06-29 09"
            },
            {
              count: 932,
              time: "2020-06-29 10"
            }
          ];
          this.$store.state.center = [
            {
              count: 776,
              time: "2020-06-29 06"
            },
            {
              count: 12,
              time: "2020-06-29 07"
            },
            {
              count: 358,
              time: "2020-06-29 08"
            },
            {
              count: 784,
              time: "2020-06-29 09"
            },
            {
              count: 345,
              time: "2020-06-29 10"
            },
            {
              count: 236,
              time: "2020-06-29 11"
            },
            {
              count: 235,
              time: "2020-06-29 12"
            },
            {
              count: 982,
              time: "2020-06-29 13"
            },
            {
              count: 198,
              time: "2020-06-29 14"
            },
            {
              count: 568,
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
              count: 347,
              time: "2020-06-29 18"
            }
          ];
          this.$store.state.bottomL = [
            { value: 213, name: "直接访问" },
            { value: 233, name: "邮件营销" },
            { value: 644, name: "联盟广告" }
          ];
          this.$store.state.bottomR = [563, 432, 678, 124, 488, 1223, 432];
          this.$store.state.show = true;
        }, 0);
      }
    }
    // mapDataEcharts() {
    //   this.$nextTick(function() {
    //     var map = Echarts.init(document.getElementById("map"));
    //     let option = {
    //       series: [
    //         {
    //           type: "map",
    //           map: "china"
    //         }
    //       ]
    //     };
    //   });
    // }
  }
};
</script>
<style lang="less" scoped>
.mapBox {
  width: 100%;
  height: 100vh;
  .mapbuttom {
    position: absolute;
    top: 200px;
    left: 10%;
  }
}
</style>