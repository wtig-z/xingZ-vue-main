<template>
  <!-- <div class="styled">Hello, Vue with LESS!</div> -->
  <!-- Header开始 -->

  <div class="affix-container">
    <!-- 检查 target 的设置 -->
    <el-affix :offset="0">
      <div class="header">
        <div class="header-container">
          <div class="nav-menu">
            <div class="left-header">
              <div class="title">
                <span><a href="#">行舟旅游网站</a></span>
              </div>
              <div class="nav-items">
                <span><a href="#">首页</a></span>
                <span><a href="#">目的地</a></span>
                <span><a href="#">旅游产品</a></span>
                <span><a href="#">关于我们</a></span>
                <span><a href="#">更多内容</a></span>
              </div>
            </div>

            <div class="search">
              <el-autocomplete
                v-model="state1"
                :fetch-suggestions="querySearch"
                placeholder="请输入内容"
                @select="handleSelect"
                @focus="clearInput"
                size="small"
              ></el-autocomplete>
              <p>{{ $t("message.hello") }}</p>
            </div>

            <div class="right-header">
              <div class="userImage"></div>
            </div>
          </div>
        </div>
      </div>
    </el-affix>
  </div>

  <!-- <div class="header">
    <div class="header-container">
      <div class="left-header">
        <div class="title"><span>旅游网站</span></div>
        <span>首页</span>
        <span>目的地</span>
        <span>旅游产品</span>
        <span>关于我们</span>
        <span>更多内容</span>
      </div>
      <div class="right-header">
        <div class="right-header-img-1"></div>
        <div class="right-header-img-2"></div>
      </div>
    </div>
  </div> -->
  <!-- Header结束 -->

  <!-- Main开始 -->
  <div class="main-part-1">
    <div class="main-part1-container">
      <div class="part1-left">
        <div class="left-forehead">
          <div class="txt1">旅游目的地</div>
          <div class="txt2">
            欢迎来到我们的旅游目的地页面，这里有丰富的旅游资源等待你的探索。
          </div>
        </div>
        <div class="place-search-panel">
          <h2>Don't fear the unknown</h2>
          <form action="search-form" method="get">
            <div class="searchbar">
              <input
                class="search-input"
                autocomplete="off"
                type="text"
                name="q"
                placeholder="我想去"
              />
              <a class="search-button" href="#" data-cs-l="搜索" role="button">
                <i class="icon-search"></i>
              </a>
            </div>
            <div></div>
          </form>
          <div class="places-search-hot">
            <a href="/travel-scenic-spot/mafengwo/10065.html">北京</a>
            <a href="/travel-scenic-spot/mafengwo/10088.html">广州</a>
            <a href="/travel-scenic-spot/mafengwo/10207.html">苏州</a>
            <a href="/travel-scenic-spot/mafengwo/10208.html">重庆</a>
            <a href="/travel-scenic-spot/mafengwo/10466.html">长沙</a>
          </div>
        </div>
        <div class="left-bottom">
          <div class="button1">
            <div class="button1-txt">查看更多</div>
          </div>
          <div>
            <div class="button2">
              <div class="button2-txt">在线预订</div>
            </div>
          </div>
        </div>
      </div>
      <div class="show-info">
        <div class="show-name">
          <a
            href="https://www.mafengwo.cn/gonglve/ziyouxing/302680.html"
            target="_blank"
          >
            <h2>神仙海岛得三款热门玩法，去普吉一定不能错过</h2>
          </a>
        </div>
        <p class="txt">
          关于泰国普吉岛，这个多面风情的岛屿，常年位于境外旅游热搜榜前列，第一次去的人，容易被它的热带海岛风情和高性价比吸引到想再二刷；第N次去的人，更是因为每次都能发现普吉的新玩法，让人想再多宠幸一遍。
        </p>
        <div class="show-links">
          <a
            href="http://www.mafengwo.cn/gonglve/ziyouxing/302680.html"
            target="_blank"
            >阅读全文</a
          >
        </div>
      </div>
    </div>
  </div>

  <div class="hot-point">
    <div class="h-title">
      <h1>热门目的地</h1>
    </div>
    <div class="h-container">
      <el-row>
        <el-col :span="12">
          <div class="region">
            <el-row>
              <el-col :span="6" style="font-size:16px ;font-family: Arial;"> 直辖市 </el-col>
              <el-col :span="12">北京 上海 重庆 天津 </el-col>
            </el-row>
          </div>
        </el-col>
        <el-col :span="12">
          <el-row class="region">
            <el-col :span="6" style="font-size:16px ;font-family: Arial;">西藏 贵州</el-col>
            <el-col :span="12"> 拉萨 林芝 阿里 黔东南 </el-col>
          </el-row>
        </el-col>

        <el-col :span="12">
          <el-row class="region">
            <el-col :span="6" style="font-size:16px ;font-family: Arial;">云南</el-col>

            <el-col :span="12"
              >丽江 大理 昆明 香格里拉 泸沽湖 双廊 西双版纳 束河 腾冲
              雨崩</el-col
            >
          </el-row>
        </el-col>

        <el-col :span="12">
          <el-row class="region">
            <el-col :span="6" style="font-size:16px ;font-family: Arial;">西北</el-col>
            <el-col :span="12"
              >西安 青海湖 西宁 祁连 敦煌 兰州 甘南 张掖 嘉峪关 新疆</el-col
            >
          </el-row>
        </el-col>

        <el-col :span="12">
          <el-row class="region">
            <el-col :span="6" style="font-size:16px ;font-family: Arial;">四川</el-col>

            <el-col :span="12"
              >成都 九寨沟 稻城 色达 若尔盖 都江堰 亚丁 阿坝 峨眉山
              牛背山</el-col
            >
          </el-row>
        </el-col>

        <el-col :span="12" >
          <el-row class="region">
            <el-col :span="6" style="font-size:16px ;font-family: Arial;">山东 山西</el-col>
            <el-col :span="12"
              >青岛 泰山 日照 威海 烟台 长岛 蓬莱 平遥 大同 五台山
              壶口瀑布</el-col
            >
          </el-row>
        </el-col>

        <el-col :span="12" >
          <el-row class="region">
            <el-col :span="6" style="font-size:16px ;font-family: Arial;">浙江</el-col>
            <el-col :span="12"
              >杭州 乌镇 西塘 千岛湖 普陀山 东极岛 南浔
            </el-col>
          </el-row>
        </el-col>

        <el-col :span="12">
          <el-row class="region">
            <el-col :span="6" style="font-size:16px ;font-family: Arial;">湖南 湖北</el-col>
            <el-col :span="12">张家界 凤凰 郴州 武汉 恩施 神农架</el-col>
          </el-row>
        </el-col>
        <el-col :span="12">
          <el-row class="region">
            <el-col :span="6" style="font-size:16px ;font-family: Arial;">海南 福建 </el-col>
            <el-col :span="14"
              >三亚 蜈支洲岛 海口 厦门 鼓浪屿 武夷山 泉州</el-col
            >
          </el-row>
        </el-col>
        <el-col :span="12">
          <el-row class="region">
            <el-col :span="6" style="font-size:16px ;font-family: Arial;">安徽 江西</el-col>
            <el-col :span="12">黄山 宏村 婺源 景德镇 庐山 三清山 南昌</el-col>
          </el-row>
        </el-col>
        <el-col :span="12">
          <el-row class="region">
            <el-col :span="6" style="font-size:16px ;font-family: Arial;">江苏</el-col>
            <el-col :span="12"
              >南京 苏州 无锡 扬州 周庄 常州 连云港 同里</el-col
            >
          </el-row>
        </el-col>
        <el-col :span="12">
          <el-row class="region">
            <el-col :span="6" style="font-size:16px ;font-family: Arial;">河北 河南</el-col>
            <el-col :span="12"
              >北戴河 秦皇岛 承德 张北 少林寺 洛阳 龙门石窟</el-col
            >
          </el-row>
        </el-col>
        <el-col :span="12">
          <el-row class="region">
            <el-col :span="6" style="font-size:16px ;font-family: Arial;">广东 广西</el-col>
            <el-col :span="12"
              >广州 深圳 珠海 汕头 桂林 阳朔 北海 黄姚古镇 涠洲岛
              龙脊梯田</el-col
            >
          </el-row>
        </el-col>
        <el-col :span="12">
          <el-row class="region"> 
            <el-col :span="6" style="font-size:16px ;font-family: Arial;">内蒙古 东北</el-col>
            <el-col :span="12"
              >呼伦贝尔 阿尔山 海拉尔 哈尔滨 漠河 雪乡 大连 丹东 盘锦</el-col
            >
          </el-row>
        </el-col>
      </el-row>
      <div class="hc-left"></div>
      <div class="hc-right"></div>
    </div>
  </div>

  <div class="main-part-4">
    <div class="warp">
      <div class="part1-right" style="position: relative; left: 100px">
        <TextComponent />
      </div>
    </div>
  </div>

  <div class="main-part-2">
    <div class="part2-title">
      <span class="title-txt">热门景点</span>
    </div>
    <div class="wrap">
      <div class="part2-container">
        <div class="part2-nav">
          <div class="nav-left">
            <div class="nav1"><span class="nav1-txt">国内</span></div>
            <div class="nav2"><span class="nav2-txt">亚洲</span></div>
            <div class="nav3"><span class="nav3-txt">欧洲</span></div>
            <div class="nav4"><span class="nav4-txt">美洲</span></div>
            <div class="nav5"><span class="nav5-txt">大洋洲</span></div>
          </div>
          <div class="nav-right">
            <div class="nr-button1"><span class="nrb1-txt">全部</span></div>
            <div class="nr-button2"><span class="nrb2-txt">自然风光</span></div>
          </div>
        </div>
        <div class="pc2-bottom">
          <div class="pc2-bottom-top">
            <div class="pc2-bottom-top-item1">
              <div class="img-pc2"></div>
              <div class="text-pc2">
                <div class="text1-pc2">张家界 许晓超</div>
                <div class="text2-pc2">
                  <div class="img-And"></div>
                  <div class="img-text">湖南省张家界市</div>
                </div>
              </div>
            </div>
            <div class="pc2-bottom-top-item2">
              <div class="img-pc2"></div>
              <div class="text-pc2">
                <div class="text1-pc2">张家界 许晓超</div>
                <div class="text2-pc2">
                  <div class="img-And"></div>
                  <div class="img-text">湖南省张家界市</div>
                </div>
              </div>
            </div>
            <div class="pc2-bottom-top-item3">
              <div class="img-pc2"></div>
              <div class="text-pc2">
                <div class="text1-pc2">张家界 许晓超</div>
                <div class="text2-pc2">
                  <div class="img-And"></div>
                  <div class="img-text">湖南省张家界市</div>
                </div>
              </div>
            </div>
            <!-- <div class="pc2-bottom-top-item4">
            <div class="img-pc2"></div>
            <div class="text-pc2">
              <div class="text1-pc2">张家界 许晓超</div>
              <div class="text2-pc2">
                <div class="img-And"></div>
                <div class="img-text">湖南省张家界市</div>
              </div>
            </div>
          </div> -->
          </div>
        </div>

        <div class="pc2-bottom">
          <div class="pc2-bottom-top">
            <div class="pc2-bottom-top-item1">
              <div class="img-pc2"></div>
              <div class="text-pc2">
                <div class="text1-pc2">张家界 许晓超</div>
                <div class="text2-pc2">
                  <div class="img-And"></div>
                  <div class="img-text">湖南省张家界市</div>
                </div>
              </div>
            </div>
            <div class="pc2-bottom-top-item2">
              <div class="img-pc2"></div>
              <div class="text-pc2">
                <div class="text1-pc2">张家界 许晓超</div>
                <div class="text2-pc2">
                  <div class="img-And"></div>
                  <div class="img-text">湖南省张家界市</div>
                </div>
              </div>
            </div>
            <div class="pc2-bottom-top-item3">
              <div class="img-pc2"></div>
              <div class="text-pc2">
                <div class="text1-pc2">张家界 许晓超</div>
                <div class="text2-pc2">
                  <div class="img-And"></div>
                  <div class="img-text">湖南省张家界市</div>
                </div>
              </div>
            </div>
            <!-- <div class="pc2-bottom-top-item4">
            <div class="img-pc2"></div>
            <div class="text-pc2">
              <div class="text1-pc2">张家界 许晓超</div>
              <div class="text2-pc2">
                <div class="img-And"></div>
                <div class="img-text">湖南省张家界市</div>
              </div>
            </div>
          </div> -->
          </div>

          <!-- <div class="pc2-bottom-bottom">
             <div class="pc2-bottom-top-item5">
            <div class="img-pc2"></div>
            <div class="text-pc2">
              <div class="text1-pc2">张家界 许晓超</div>
              <div class="text2-pc2">
                <div class="img-And"></div>
                <div class="img-text">1111</div>
              </div>
            </div>
          </div>
          <div class="pc2-bottom-top-item6">
            <div class="img-pc2"></div>
            <div class="text-pc2">
              <div class="text1-pc2">张家界 许晓超</div>
              <div class="text2-pc2">
                <div class="img-And"></div>
                <div class="img-text"></div>
              </div>
            </div>
          </div>
          <div class="pc2-bottom-top-item7">
            <div class="img-pc2"></div>
            <div class="text-pc2">
              <div class="text1-pc2">张家界 许晓超</div>
              <div class="text2-pc2">
                <div class="img-And"></div>
                <div class="img-text"></div>
              </div>
            </div>
          </div>
          <div class="pc2-bottom-top-item8">
            <div class="img-pc2"></div>
            <div class="text-pc2">
              <div class="text1-pc2">张家界 许晓超</div>
              <div class="text2-pc2">
                <div class="img-And"></div>
                <div class="img-text"></div>
              </div>
            </div>
          </div>
        </div> -->

          <!-- <div class="pc2b-forehead">
          <div class="item1">
            <div class="item1-img"></div>
            <div class="item1-txt">
              <div class="it1-txt1">
                <span class="item1-txt1-1">张家界</span>
                <span class="item1-txt1-2">许晓超</span>
              </div>
              <div class="it1-txt2">
                <div class="item1-txt2-icon"></div>
                <div class="item1-txt2-2">湖南省张家界市</div>
              </div>
            </div>
          </div>
          <div class="item2">
            <div class="item2-img"></div>
            <div class="item2-txt">
              <div class="it2-txt1">
                <span class="item2-txt1-1">张家界</span>
                <span class="item2-txt1-2">许晓超</span>
              </div>
              <div class="it2-txt2">
                <div class="item2-txt2-icon"></div>
                <div class="item2-txt2-2">湖南省张家界市</div>
              </div>
            </div>
          </div>
          <div class="item3">
            <div class="item3-img"></div>
            <div class="item3-txt">
              <div class="it3-txt1">
                <span class="item3-txt1-1">张家界</span>
                <span class="item3-txt1-2">许晓超</span>
              </div>
              <div class="it3-txt2">
                <div class="item3-txt2-icon"></div>
                <div class="item3-txt2-2">湖南省张家界市</div>
              </div>
            </div>
          </div>
          <div class="item4">
            <div class="item4-img"></div>
            <div class="item4-txt">
              <div class="it4-txt1">
                <span class="item4-txt1-1">张家界</span>
                <span class="item4-txt1-2">许晓超</span>
              </div>
              <div class="it4-txt2">
                <div class="item4-txt2-icon"></div>
                <div class="item4-txt2-2">湖南省张家界市</div>
              </div>
            </div>
          </div>
        </div>
        <div class="pc2b-bottom">
          <div class="item5">
            <div class="item5-img"></div>
            <div class="item5-txt">
              <div class="it5-txt1">
                <span class="item5-txt1-1">张家界</span>
                <span class="item5-txt1-2">许晓超</span>
              </div>
              <div class="it5-txt2">
                <div class="item5-txt2-icon"></div>
                <div class="item5-txt2-2">湖南省张家界市</div>
              </div>
            </div>
          </div>
          <div class="item6">
            <div class="item6-img"></div>
            <div class="item6-txt">
              <div class="it6-txt1">
                <span class="item6-txt1-1">张家界</span>
                <span class="item6-txt1-2">许晓超</span>
              </div>
              <div class="it6-txt2">
                <div class="item6-txt2-icon"></div>
                <div class="item6-txt2-2">湖南省张家界市</div>
              </div>
            </div>
          </div>
          <div class="item7">
            <div class="item7-img"></div>
            <div class="item7-txt">
              <div class="it7-txt1">
                <span class="item7-txt1-1">张家界</span>
                <span class="item7-txt1-2">许晓超</span>
              </div>
              <div class="it7-txt2">
                <div class="item7-txt2-icon"></div>
                <div class="item7-txt2-2">湖南省张家界市</div>
              </div>
            </div>
          </div>
          <div class="item8">
            <div class="item8-img"></div>
            <div class="item8-txt">
              <div class="it8-txt1">
                <span class="item8-txt1-1">张家界</span>
                <span class="item8-txt1-2">许晓超</span>
              </div>
              <div class="it8-txt2">
                <div class="item8-txt2-icon"></div>
                <div class="item8-txt2-2">湖南省张家界市</div>
              </div>
            </div>
          </div>
        </div> -->
        </div>
      </div>
    </div>
  </div>
  <div class="main-part-3">
    <div class="part3-left">
      <div class="p3l-forehead">目的地介绍</div>
      <div class="p3l-center">
        欢迎来到我们的目的地页面！在这里，你可以找到各种热门景点的介绍和推荐。无论你是喜欢自然风光、历史文化、城市风光，还是喜欢冒险探险、美食美景、海滩度假、山水风光，我们都能满足你的需求。快来探索各个目的地，寻找你心仪的旅游目的地吧！
      </div>
      <div class="p3l-bottom">
        <div class="p3lb-box">
          <div class="box-txt">查看更多</div>
          <div class="p3lb-icon"></div>
        </div>
      </div>
    </div>
    <div class="part3-right"></div>
  </div>
  <!-- Main结束 -->

  <!-- Footer开始 -->
  <div class="wrap">
    <div class="footer">
      <div class="footer-forehead">
        <div class="footer-forehead-left">
          <div class="top">
            <div class="txt">
              <span>旅游网</span>
            </div>
            <div class="img"></div>
            <div class="txt-2">发现更多精彩旅程</div>
            <div class="e-mail">
              <div class="input-box">
                <div class="input-txt">请输入邮箱地址</div>
              </div>
              <div class="e-mail-icon">
                <div class="icon-describe">订阅</div>
              </div>
            </div>
          </div>
        </div>
        <div class="footer-forehead-center">
          <div class="ffc1">
            <div class="ffc1-head">关于我们</div>
            <div class="ffc1-container">
              <div>项目简介</div>
              <div>联系我们</div>
              <div>合作伙伴</div>
            </div>
          </div>
          <div class="ffc2">
            <div class="ffc2-head">帮助中心</div>
            <div class="ffc2-container">
              <div>常见问题</div>
              <div>使用指南</div>
              <div>用户反馈</div>
            </div>
          </div>
        </div>
        <div class="footer-forehead-right">
          <div class="right-txt">关注我们</div>
          <div class="right-icon">
            <div class="icon-1"></div>
            <div class="icon-2"></div>
          </div>
        </div>
      </div>
      <div class="footer-bottom">
        <div class="footer-bottom-container-head"></div>
        <div class="footer-bottom-container">
          <div class="footer-left">
            <span>©2024 产品版权所有。保留所有权利。</span>
          </div>
          <div class="footer-right">
            <span>隐私政策</span>
            <span>服务条款</span>
            <span>Cookie设置</span>
          </div>
        </div>
      </div>
    </div>
  </div>

  <!-- Footer结束 -->
</template>
  
  <script>
import { defineComponent } from "vue";
// 引入 Element Plus 组件
import {
  ElContainer,
  ElHeader,
  ElAside,
  ElMain,
  ElFooter,
  ElRow,
  ElCol,
} from "element-plus";
import TextComponent from "@/components/TextComponent.vue";

export default defineComponent({
  name: "App",
  components: {
    ElContainer,
    ElHeader,
    ElAside,
    ElMain,
    ElFooter,
    ElRow,
    ElCol,
    TextComponent, // 注册 TextComponent 组件
  },
});
</script>
  
  
  <style lang="less">

  
// 定义通用变量
@color-primary: rgba(29, 33, 41, 1);
@font-kalam-bold: "Kalam-Bold";
@font-harmony: "HarmonyOSSansSC-Regular";
@bg-color: white;
@box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
@header-height: 72px;
@container-width: 1200px;
@user-img-url: url("/src/assets/6556e75090ab84325baa614a.png");


.region {
    padding-bottom: 20px;
  }
.affix-container {
  width: 100%;
  margin: 0 auto;

  /* 设置最小宽度 */

  a {
    color: black;
  }
  
  .header {
    width: 100%;
    height: @header-height;
    z-index: 1000; // 确保导航栏在其他元素之上
    background-color: @bg-color; // 背景颜色
    box-shadow: @box-shadow; // 添加阴影
    display: flex;
    justify-content: center;
    align-items: center;
    box-sizing: border-box;

    .header-container {
      position: relative;
      width: 100%;
      max-width: @container-width;
      min-width: @container-width;
      height: @header-height;
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 0 20px;
      box-sizing: border-box;

      .nav-menu {
        display: flex;
        justify-content: space-between;
        align-items: center;
        width: 100%;

        .left-header {
          display: flex;
          align-items: center;
          gap: 60px;

          .title {
            color: @color-primary;
            font-size: 22px;
            font-weight: 700;
            font-family: @font-kalam-bold;
            white-space: nowrap;
          }

          .nav-items {
            display: flex;
            gap: 32px;

            span {
              color: @color-primary;
              font-size: 16px;
              line-height: 24px;
              font-weight: 400;
              font-family: @font-harmony;
              white-space: nowrap;
            }
          }
        }

        .search {
          display: flex;
          align-items: center;
          gap: 10px;
        }

        .right-header {
          display: flex;
          align-items: center;
          gap: 24px;

          .userImage {
            width: 40px;
            height: 40px;
            background-image: var(--bg-img);
            background-position: center;
            background-size: cover;
            background-repeat: no-repeat;
            border-radius: 50%;
            --bg-img: var(--img-url);
            --img-url: @user-img-url;
          }
        }
      }
    }
  }
}

.main-part-4 {
  top: 350px;
  position: relative;
  .warp {
    margin: 0 auto;
    width: 1200px;
    min-width: 1200px;
    max-width: 1200px;
    gap: 20px;
    //   .part1-right{
    // position: relative;
    //       z-index: 2;
    //       width: 680px;
    //       height: 1080px;
    //       mix-blend-mode: normal;
    //       display: flex;
    //       order: 1;
    //       flex-shrink: 0;
    //       overflow: hidden; /* 确保内容不会溢出 */
    //       justify-content: center;
    //       align-items: center; /* 中心对齐内容 */

    // }
  }
}

.styled {
  color: #333;
  background-color: lighten(#f06, 10%);
}

/* Header开始 */
.header {
  position: relative;
  z-index: 1;
  width: 100%;
  height: 72px;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 0 80px;
  box-sizing: border-box;

  .header-container {
    position: relative;
    z-index: 1;
    width: 100%;
    display: flex;
    justify-content: space-between;
    align-items: center;

    .left-header {
      display: flex;
      gap: 20px;

      .title {
        color: #1d2129;
        font-size: 22px;
        font-weight: bold;
      }
    }

    .right-header {
      display: flex;
      gap: 24px;

      .right-header-img-1,
      .right-header-img-2 {
        width: 40px;
        height: 40px;
        border-radius: 50%;
        background-size: cover;
        background-position: center;
      }

      .right-header-img-1 {
        background-image: url("https://img.jsdesign2.com/assets/img/6556e73fe1e45fa4efce1420.png#af9528f906d97ad9c68164f4572a6ec4");
      }

      .right-header-img-2 {
        background-image: url("https://img.jsdesign2.com/assets/element/js_t5Ay7g8MlE0/image/3e260053f3fe1a53d64fd219a5465acdad443bce.png");
      }
    }
  }
}
/* Header样式结束 */

/* Main样式开始*/
.main-part-1 {
  background-image: url("../assets/destinationBanner.jpg");
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center;
  height: 689px;

  position: relative;
  z-index: 2;
  width: unset;

  mix-blend-mode: normal;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: center;
  padding: 80px 80px 80px 80px;
  overflow: hidden;
  box-sizing: border-box;
  gap: 80px;
  order: 1;
  min-height: auto;
  align-self: stretch;
  .main-part1-container {
    position: relative;
    z-index: 1;
    width: 1280px;
    height: auto;
    mix-blend-mode: normal;
    display: flex;
    justify-content: flex-start;
    align-items: center;
    gap: 80px;
    order: 0;
    min-height: auto;
    .part1-left {
      position: relative;
      z-index: 1;
      width: unset;
      height: auto;
      mix-blend-mode: normal;
      display: flex;
      flex-direction: column;
      justify-content: flex-start;
      align-items: flex-start;
      gap: 24px;
      order: 0;
      flex: 1;
      .left-forehead {
        position: relative;
        z-index: 1;
        width: unset;
        height: auto;
        mix-blend-mode: normal;
        display: flex;
        flex-direction: column;
        justify-content: flex-start;
        align-items: flex-start;
        gap: 24px;
        order: 0;
        min-height: auto;
        align-self: stretch;
        .txt1 {
          position: relative;
          left: 50px;
          display: flex;
          flex-direction: column;
          z-index: 0;
          justify-content: start;
          width: unset;
          mix-blend-mode: normal;
          color: rgb(247, 247, 247);
          font-size: 56px;
          line-height: 66px;
          font-weight: 700;
          opacity: 1;
          font-family: "HarmonyOSSansSC-Bold";
          letter-spacing: 0px;
          white-space: pre-wrap;
          order: 0;
          height: auto;
          align-self: stretch;
        }
        .txt2 {
          position: relative;
          left: 48px;
          text-align: left;
          display: flex;
          flex-direction: column;
          z-index: 1;
          justify-content: start;
          width: unset;
          mix-blend-mode: normal;
          color: rgb(247, 247, 247);
          font-size: 18px;
          line-height: 28px;
          font-weight: 400;
          opacity: 1;
          font-family: "HarmonyOSSansSC-Regular";
          letter-spacing: 0px;
          // white-space: pre-wrap;
          order: 1;
          height: auto;
          align-self: stretch;
        }
      }
      .place-search-panel {
        position: relative;
        left: 50px;
        h2 {
          font-size: 20px;
          color: rgb(247, 247, 247);
          margin-bottom: 15px;
          font-weight: normal;
          line-height: 1;
          font-family: "Microsoft Yahei";
        }
        form {
          display: block;
          margin-top: 0em;
          unicode-bidi: isolate;
          .search-input {
            height: 46px;
            width: 348px;
          }
          .icon-search {
            display: inline-block;
            margin-top: 7px;
            width: 50px;
            height: 50px;
            background: url("../assets/基础-搜素 (1).png") no-repeat center /
              50px 50px;
            overflow: hidden;
            vertical-align: top;
            position: relative;
            top: -10px;
            left: 20px;
          }
        }
        .places-search-hot {
          a {
            margin-right: 10px;
            color: rgb(247, 247, 247);
          }
        }
      }
      .left-bottom {
        position: relative;
        left: 50px;
        z-index: 2;
        width: 208px;
        height: auto;
        mix-blend-mode: normal;
        display: flex;
        justify-content: flex-start;
        align-items: flex-start;
        padding: 16px 0px 0px 0px;
        box-sizing: border-box;
        gap: 16px;
        order: 1;
        min-height: auto;
        .button1 {
          position: relative;
          z-index: 1;
          width: auto;
          height: 52px;
          border-radius: 4px;
          mix-blend-mode: normal;
          display: flex;
          justify-content: center;
          align-items: center;
          padding: 0px 24px 0px 24px;
          background: rgba(0, 89, 255, 1);
          box-sizing: border-box;
          gap: 8px;
          order: 0;
          min-width: auto;
          .button1-txt {
            color: rgba(255, 255, 255, 1);
            font-size: 20px;
            line-height: 32px;
            font-weight: 400;
            font-family: "HarmonyOSSansSC-Regular";
            letter-spacing: 0px;
            white-space: nowrap;
          }
        }
        .button2 {
          position: relative;
          z-index: 2;
          width: auto;
          height: 52px;
          border-radius: 4px;
          mix-blend-mode: normal;
          display: flex;
          justify-content: center;
          align-items: center;
          padding: 0px 24px 0px 24px;
          opacity: 1;
          background: rgba(255, 255, 255, 1);
          box-sizing: border-box;
          gap: 8px;
          order: 1;
          min-width: auto;
          border: solid 1px black;
          .button2-txt {
            color: rgba(29, 33, 41, 1);
            font-size: 20px;
            line-height: 32px;
            font-weight: 400;
            font-family: "HarmonyOSSansSC-Regular";
            letter-spacing: 0px;
            white-space: nowrap;
          }
        }
      }
    }
    .show-info {
      margin-top: -120px;
      padding-right: 30px;
      // border-right: 7px solid #100f0f;
      width: 550px;
      height: 285px;
      text-shadow: 0 2px 3px rgba(0, 0, 0, 0.5);
      color: rgb(247, 247, 247);
      font-size: 16px;
      line-height: 1.8;
      white-space: normal;
      text-align: left;
      margin-right: 100px;
      .show-name {
        position: static;
        margin: 10px 0;
        font-size: 40px;
        line-height: 1.3;
        text-align: left;
        a {
          color: rgb(247, 247, 247); /* 将超链接的颜色更改为黑色 */
          text-decoration: none; /* 可选：移除下划线，如果你也不想要下划线的话 */
        }

        /* 如果你还想为鼠标悬停在链接上时改变颜色，可以这样做： */
        a:hover {
          color: #ffd000; /* 鼠标悬停时链接颜色变为红色 */
        }
        h2 {
          font-weight: normal;
          line-height: inherit;
        }

        .txt {
          top: 130px;
          right: 140px;
          font-size: 18px;
        }
      }
      .show-links {
        position: static;
        display: inline-block;
        margin-top: 10px;
        color: rgb(247, 247, 247);
        text-decoration: underline;
        font-size: 24px;
        a {
          color: rgb(247, 247, 247); /* 将超链接的颜色更改为黑色 */
          text-decoration: none; /* 可选：移除下划线，如果你也不想要下划线的话 */
        }

        /* 如果你还想为鼠标悬停在链接上时改变颜色，可以这样做： */
        a:hover {
          color: #ffd000; /* 鼠标悬停时链接颜色变为红色 */
        }
      }
    }
    //   .picture1 {
    //     position: absolute;
    //     z-index: 0;
    //     left: 20px;
    //     top: 20px;
    //     width: 480px;
    //     height: 640px;
    //     border-radius: 8px;
    //     mix-blend-mode: normal;
    //     box-sizing: border-box;
    //     opacity: 1;

    //     background-image: url(https://img.jsdesign2.com/assets/img/6556e73f90ab84325baa606a.png#85d85dbadb9db0744eaa6c894d882c4d);
    //   }
    //   .picture2 {
    //     position: absolute;
    //     z-index: 1;
    //     left: 60px;
    //     top: 20px;
    //     width: 480px;
    //     height: 640px;
    //     border-radius: 8px;
    //     mix-blend-mode: normal;
    //     box-sizing: border-box;
    //     opacity: 1;

    //     background-image: url(https://img.jsdesign2.com/assets/img/6556e738a12e5e2687bbec56.png#4d29663c6a133d50c1c1d2a70c0988a1);
    //   }
    //   .picture3 {
    //     position: absolute;
    //     z-index: 2;
    //     left: 100px;
    //     top: 20px;
    //     width: 480px;
    //     height: 640px;
    //     border-radius: 8px;
    //     mix-blend-mode: normal;
    //     box-sizing: border-box;
    //     opacity: 1;

    //     background-image: url(https://img.jsdesign2.com/assets/img/6556e73109dc60275483cac2.png#a5614229ed4a88f45748333e152c8413);
    //   }
    //   .picture4 {
    //     position: absolute;
    //     z-index: 3;
    //     left: 140px;
    //     top: 20px;
    //     width: 480px;
    //     height: 640px;
    //     border-radius: 8px;
    //     mix-blend-mode: normal;
    //     box-sizing: border-box;
    //     opacity: 1;

    //     background-image: url(https://img.jsdesign2.com/assets/img/6556e740eb009f7cc7031d9c.png#eb9b1f394997e92225fd6ce1067cddf2);
    //   }
    //   .picture5 {
    //     position: absolute;
    //     z-index: 4;
    //     left: 180px;
    //     top: 20px;
    //     width: 480px;
    //     height: 640px;
    //     border-radius: 8px;
    //     mix-blend-mode: normal;
    //     box-sizing: border-box;
    //     opacity: 1;

    //     background-image: url(https://img.jsdesign2.com/assets/img/65374fa6ccc9429bf6ded8c1.png#a538c274220a418dcb396bc184e07ba7);
    //   }
    // }
    //     .part1-right {
    //   display: flex;
    //   justify-content: center;
    //   align-items: center;
    //   height: 100%;
    // }
    .part1-right {
      position: relative;

      left: 100px;

      top: 300px;
      z-index: 2;
      width: 680px;
      height: 1080px;
      mix-blend-mode: normal;
      display: flex;
      order: 1;
      flex-shrink: 0;
      overflow: hidden; /* 确保内容不会溢出 */
      //justify-content: center;
      //align-items: center; /* 中心对齐内容 */
    }

    .cards-container {
      width: 2000px;
      display: flex;
      flex-wrap: wrap;

      justify-content: center;
      transform: scale(0.7); /* 调整缩放比例，确保卡片适应容器 */
      transform-origin: center; /* 缩放中心 */
      gap: 10px; /* 卡片之间的间距 */
    }

    .card {
      margin-right: 30px;
      margin: 5px;
      width: auto; /* 调整卡片宽度以适应容器 */
      height: auto;
      box-sizing: border-box;
      /* 其他样式保持不变 */
    }
  }
}
.hot-point {
  width: 1000px;
  margin: 0 auto;
  .h-title {
    margin-bottom: 35px;
    text-align: center;
    font-size: 16px;
    line-height: 24px;
  }
  .h-container {
    line-height: 24px;
    font-size: 14px;
    .hc-left {
      float: left;
      width: 470px;
      dt {
        float: left;
        font-size: 16px;
        color: #333;
        margin-left: -100px;
      }
    }
    .hc-right {
      margin-left: 60px;
    }
  }
}
.main-part-2 {
  position: relative;
  top: 400px;
  z-index: 3;
  width: 100%;
  max-width: 1200px;
  /* 设置最小宽度 */
  max-width: 1200px;
  margin: 0 auto;
  mix-blend-mode: normal;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: center;
  padding: 80px 80px 80px 80px;
  overflow: hidden;
  box-sizing: border-box;
  gap: 64px;
  order: 2;
  min-height: auto;
  align-self: stretch;
  .part2-title {
    position: relative;
    display: flex;
    flex-direction: column;
    z-index: 0;
    justify-content: start;
    width: unset;
    mix-blend-mode: normal;
    color: rgba(29, 33, 41, 1);
    font-size: 48px;
    line-height: 56px;
    font-weight: 700;
    opacity: 1;
    font-family: "HarmonyOSSansSC-Bold";
    letter-spacing: 0px;
    white-space: pre-wrap;
    order: 0;
    height: auto;
    align-self: stretch;
    .title-txt {
      color: rgba(29, 33, 41, 1);
      font-size: 48px;
      line-height: 56px;
      font-weight: 700;
      font-family: "HarmonyOSSansSC-Bold";
      letter-spacing: 0px;
      white-space: pre-wrap;
      position: relative;
      left: -70px;
    }
  }
  .wrap {
    width: 100%;
    max-width: 1200px;
    /* 设置最小宽度 */
    max-width: 1200px;
    margin: 0 auto;
    .part2-container {
      left: -120px;
      position: relative;
      z-index: 2;
      width: 1280px;
      height: auto;
      mix-blend-mode: normal;
      display: flex;
      flex-direction: column;
      justify-content: flex-start;
      align-items: flex-start;
      gap: 24px;
      order: 1;
      min-height: auto;
      .part2-nav {
        position: relative;
        left: 50px;
        z-index: 1;
        width: unset;
        height: auto;
        mix-blend-mode: normal;
        display: flex;
        justify-content: flex-start;
        align-items: center;
        gap: 80px;
        order: 0;
        min-height: auto;
        align-self: stretch;
        .nav-left {
          position: relative;
          z-index: 1;
          width: unset;
          height: auto;
          mix-blend-mode: normal;
          display: flex;
          justify-content: flex-start;
          align-items: center;
          gap: 32px;
          order: 0;
          flex: 1;
          .nav1 {
            position: relative;
            display: flex;
            flex-direction: column;
            z-index: 0;
            justify-content: start;
            height: 24px;
            mix-blend-mode: normal;
            color: rgba(0, 89, 255, 1);
            font-size: 16px;
            line-height: 24px;
            font-weight: 500;
            opacity: 1;
            font-family: "HarmonyOSSansSC-Medium";
            letter-spacing: 0px;
            white-space: nowrap;
            order: 0;
            width: auto;
            .nav1-txt {
              color: rgba(0, 89, 255, 1);
              font-size: 16px;
              line-height: 24px;
              font-weight: 500;
              font-family: "HarmonyOSSansSC-Medium";
              letter-spacing: 0px;
              white-space: nowrap;
            }
          }
          .nav2 {
            position: relative;
            display: flex;
            flex-direction: column;
            z-index: 1;
            justify-content: start;
            height: 24px;
            mix-blend-mode: normal;
            color: rgba(29, 33, 41, 1);
            font-size: 16px;
            line-height: 24px;
            font-weight: 400;
            opacity: 1;
            font-family: "HarmonyOSSansSC-Regular";
            letter-spacing: 0px;
            white-space: nowrap;
            order: 1;
            width: auto;
            .nav2-txt {
              color: rgba(29, 33, 41, 1);
              font-size: 16px;
              line-height: 24px;
              font-weight: 400;
              font-family: "HarmonyOSSansSC-Regular";
              letter-spacing: 0px;
              white-space: nowrap;
            }
          }
          .nav3 {
            position: relative;
            display: flex;
            flex-direction: column;
            z-index: 2;
            justify-content: start;
            height: 24px;
            mix-blend-mode: normal;
            color: rgba(29, 33, 41, 1);
            font-size: 16px;
            line-height: 24px;
            font-weight: 400;
            opacity: 1;
            font-family: "HarmonyOSSansSC-Regular";
            letter-spacing: 0px;
            white-space: nowrap;
            order: 2;
            width: auto;
            .nav3-txt {
              color: rgba(29, 33, 41, 1);
              font-size: 16px;
              line-height: 24px;
              font-weight: 400;
              font-family: "HarmonyOSSansSC-Regular";
              letter-spacing: 0px;
              white-space: nowrap;
            }
          }
          .nav4 {
            position: relative;
            display: flex;
            flex-direction: column;
            z-index: 3;
            justify-content: start;
            height: 24px;
            mix-blend-mode: normal;
            color: rgba(29, 33, 41, 1);
            font-size: 16px;
            line-height: 24px;
            font-weight: 400;
            opacity: 1;
            font-family: "HarmonyOSSansSC-Regular";
            letter-spacing: 0px;
            white-space: nowrap;
            order: 3;
            width: auto;
            .nav4-txt {
              color: rgba(29, 33, 41, 1);
              font-size: 16px;
              line-height: 24px;
              font-weight: 400;
              font-family: "HarmonyOSSansSC-Regular";
              letter-spacing: 0px;
              white-space: nowrap;
            }
          }
          .nav5 {
            position: relative;
            display: flex;
            flex-direction: column;
            z-index: 4;
            justify-content: start;
            height: 24px;
            mix-blend-mode: normal;
            color: rgba(29, 33, 41, 1);
            font-size: 16px;
            line-height: 24px;
            font-weight: 400;
            opacity: 1;
            font-family: "HarmonyOSSansSC-Regular";
            letter-spacing: 0px;
            white-space: nowrap;
            order: 4;
            width: auto;
            .nav5-txt {
              color: rgba(29, 33, 41, 1);
              font-size: 16px;
              line-height: 24px;
              font-weight: 400;
              font-family: "HarmonyOSSansSC-Regular";
              letter-spacing: 0px;
              white-space: nowrap;
            }
          }
        }
        .nav-right {
          position: relative;
          right: 100px;
          z-index: 2;
          width: auto;
          height: auto;
          mix-blend-mode: normal;
          display: flex;
          justify-content: flex-start;
          align-items: flex-start;
          gap: 4px;
          order: 1;
          min-width: auto;
          .nr-button1 {
            position: relative;
            z-index: 1;
            width: auto;
            height: 40px;
            border-radius: 4px;
            mix-blend-mode: normal;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 0px 20px 0px 20px;
            background: rgba(51, 102, 255, 1);
            box-sizing: border-box;
            gap: 8px;
            order: 0;
            min-width: auto;
            .nrb1-txt {
              color: rgba(255, 255, 255, 1);
              font-size: 16px;
              line-height: 24px;
              font-weight: 400;
              font-family: "HarmonyOSSansSC-Regular";
              letter-spacing: 0px;
              white-space: nowrap;
            }
          }
          .nr-button2 {
            position: relative;
            z-index: 2;
            width: auto;
            height: 40px;
            border-radius: 4px;
            mix-blend-mode: normal;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 0px 20px 0px 20px;
            opacity: 1;
            background: rgba(255, 255, 255, 1);
            box-sizing: border-box;
            gap: 8px;
            order: 1;
            min-width: auto;
            border: solid 1px black;
            .nrb2-txt {
              position: relative;
              display: flex;
              flex-direction: column;
              z-index: 0;
              justify-content: start;
              height: 24px;
              mix-blend-mode: normal;
              color: rgba(29, 33, 41, 1);
              font-size: 16px;
              line-height: 24px;
              font-weight: 400;
              opacity: 1;
              font-family: "HarmonyOSSansSC-Regular";
              letter-spacing: 0px;
              white-space: nowrap;
              order: 0;
              width: auto;
            }
          }
        }
      }
      .pc2-bottom {
        left: 50px;
        position: relative;
        z-index: 1;
        width: unset;
        height: auto;
        mix-blend-mode: normal;
        display: flex;
        justify-content: flex-start;
        align-items: flex-start;
        overflow: hidden;
        gap: 12px;
        order: 0;
        min-height: auto;
        align-self: stretch;

        .pc2-bottom-top {
          position: relative;
          z-index: 1;
          width: unset;
          height: auto;
          mix-blend-mode: normal;
          display: flex;
          justify-content: flex-start;
          align-items: flex-start;
          overflow: hidden;
          gap: 126px;
          order: 0;
          min-height: auto;
          align-self: stretch;
          .pc2-bottom-top-item1 {
            position: relative;
            z-index: 1;
            width: unset;
            height: 240px;
            mix-blend-mode: normal;
            align-content: flex-start;
            order: 0;
            flex: 1;
            .img-pc2 {
              position: relative;
              z-index: 1;
              width: 311px;
              height: 180px;
              border-radius: 8px;
              mix-blend-mode: normal;
              display: flex;
              justify-content: center;
              align-items: center;
              overflow: hidden;
              order: 0;
              flex-shrink: 0;
              align-self: stretch;

              display: flex;
              background-size: cover;
              background-position: center;
              background-repeat: no-repeat;
              background-image: url(https://img.jsdesign2.com/assets/img/6556e73686711ace31ea631a.png#25ebe5445751f295b3f2a216b4622814);
              background-size: 311px 180px;
            }
            .text-pc2 {
              position: relative;
              z-index: 2;
              width: unset;
              height: auto;
              mix-blend-mode: normal;
              display: flex;
              flex-direction: column;
              justify-content: flex-start;
              align-items: flex-start;
              gap: 4px;
              order: 1;
              min-height: auto;
              align-self: stretch;
              .text1-pc2 {
                position: relative;
                z-index: 1;
                width: unset;
                height: auto;
                mix-blend-mode: normal;
                display: flex;
                justify-content: flex-start;
                align-items: flex-start;
                overflow: hidden;
                gap: 8px;
                order: 0;
                min-height: auto;
                align-self: stretch;
              }
              .text2-pc2 {
                position: relative;
                z-index: 2;
                width: unset;
                height: auto;
                mix-blend-mode: normal;
                display: flex;
                justify-content: flex-start;
                align-items: center;
                gap: 4px;
                order: 1;
                min-height: auto;
                align-self: stretch;

                .img-And {
                  position: relative;
                  z-index: 0;
                  border: unset !important;
                  box-shadow: unset;
                  width: 16px;
                  height: 16px;
                  mix-blend-mode: normal;
                  display: flex;
                  background-image: url(https://img.jsdesign2.com/assets/element/js_7tbA2BbXK7x/image/916727f446e547a123e7761fbe334216331b5ec9.png);
                  background-size: 16px 16px;
                  order: 0;
                  flex-shrink: 0;
                }
                .img-text {
                  position: relative;
                  text-align: left;
                  display: flex;
                  flex-direction: column;
                  z-index: 1;
                  justify-content: start;
                  width: 291px;
                  height: 20px;
                  mix-blend-mode: normal;
                  color: rgba(134, 144, 156, 1);
                  font-size: 14px;
                  line-height: 20px;
                  font-weight: 400;
                  opacity: 1;
                  font-family: "HarmonyOSSansSC-Regular";
                  letter-spacing: 0px;
                  white-space: pre-wrap;
                  order: 1;
                  flex-shrink: 0;
                }
              }
            }
          }
          .pc2-bottom-top-item2 {
            position: relative;
            z-index: 1;
            width: unset;
            height: 240px;
            mix-blend-mode: normal;
            align-content: flex-start;
            order: 0;
            flex: 1;
            .img-pc2 {
              position: relative;
              z-index: 1;
              width: 311px;
              height: 180px;
              border-radius: 8px;
              mix-blend-mode: normal;
              display: flex;
              justify-content: center;
              align-items: center;
              overflow: hidden;
              order: 0;
              flex-shrink: 0;
              align-self: stretch;

              display: flex;
              background-size: cover;
              background-position: center;
              background-repeat: no-repeat;
              background-image: url(https://img.jsdesign2.com/assets/img/6556e73686711ace31ea631a.png#25ebe5445751f295b3f2a216b4622814);
              background-size: 311px 180px;
            }
            .text-pc2 {
              position: relative;
              z-index: 2;
              width: unset;
              height: auto;
              mix-blend-mode: normal;
              display: flex;
              flex-direction: column;
              justify-content: flex-start;
              align-items: flex-start;
              gap: 4px;
              order: 1;
              min-height: auto;
              align-self: stretch;
              .text1-pc2 {
                position: relative;
                z-index: 1;
                width: unset;
                height: auto;
                mix-blend-mode: normal;
                display: flex;
                justify-content: flex-start;
                align-items: flex-start;
                overflow: hidden;
                gap: 8px;
                order: 0;
                min-height: auto;
                align-self: stretch;
              }
              .text2-pc2 {
                position: relative;
                z-index: 2;
                width: unset;
                height: auto;
                mix-blend-mode: normal;
                display: flex;
                justify-content: flex-start;
                align-items: center;
                gap: 4px;
                order: 1;
                min-height: auto;
                align-self: stretch;

                .img-And {
                  position: relative;
                  z-index: 0;
                  border: unset !important;
                  box-shadow: unset;
                  width: 16px;
                  height: 16px;
                  mix-blend-mode: normal;
                  display: flex;
                  background-size: 16px 16px;
                  background-image: url(https://img.jsdesign2.com/assets/element/js_7tbA2BbXK7x/image/916727f446e547a123e7761fbe334216331b5ec9.png);
                  order: 0;
                  flex-shrink: 0;
                }
                .img-text {
                  text-align: left;
                  position: relative;
                  display: flex;
                  flex-direction: column;
                  z-index: 1;
                  justify-content: start;
                  width: 291px;
                  height: 20px;
                  mix-blend-mode: normal;
                  color: rgba(134, 144, 156, 1);
                  font-size: 14px;
                  line-height: 20px;
                  font-weight: 400;
                  opacity: 1;
                  font-family: "HarmonyOSSansSC-Regular";
                  letter-spacing: 0px;
                  white-space: pre-wrap;
                  order: 1;
                  flex-shrink: 0;
                }
              }
            }
          }
          .pc2-bottom-top-item3 {
            position: relative;
            z-index: 1;
            width: unset;
            height: 240px;
            mix-blend-mode: normal;
            align-content: flex-start;
            order: 0;
            flex: 1;
            .img-pc2 {
              position: relative;
              z-index: 1;
              width: 311px;
              height: 180px;
              border-radius: 8px;
              mix-blend-mode: normal;
              display: flex;
              justify-content: center;
              align-items: center;
              overflow: hidden;
              order: 0;
              flex-shrink: 0;
              align-self: stretch;

              display: flex;
              background-size: cover;
              background-position: center;
              background-repeat: no-repeat;
              background-image: url(https://img.jsdesign2.com/assets/img/6556e73686711ace31ea631a.png#25ebe5445751f295b3f2a216b4622814);
              background-size: 311px 180px;
            }
            .text-pc2 {
              position: relative;
              z-index: 2;
              width: unset;
              height: auto;
              mix-blend-mode: normal;
              display: flex;
              flex-direction: column;
              justify-content: flex-start;
              align-items: flex-start;
              gap: 4px;
              order: 1;
              min-height: auto;
              align-self: stretch;
              .text1-pc2 {
                position: relative;
                z-index: 1;
                width: unset;
                height: auto;
                mix-blend-mode: normal;
                display: flex;
                justify-content: flex-start;
                align-items: flex-start;
                overflow: hidden;
                gap: 8px;
                order: 0;
                min-height: auto;
                align-self: stretch;
              }
              .text2-pc2 {
                position: relative;
                z-index: 2;
                width: unset;
                height: auto;
                mix-blend-mode: normal;
                display: flex;
                justify-content: flex-start;
                align-items: center;
                gap: 4px;
                order: 1;
                min-height: auto;
                align-self: stretch;

                .img-And {
                  position: relative;
                  z-index: 0;
                  border: unset !important;
                  box-shadow: unset;
                  width: 16px;
                  height: 16px;
                  mix-blend-mode: normal;
                  display: flex;
                  background-size: 16px 16px;
                  background-image: url(https://img.jsdesign2.com/assets/element/js_7tbA2BbXK7x/image/916727f446e547a123e7761fbe334216331b5ec9.png);
                  order: 0;
                  flex-shrink: 0;
                }
                .img-text {
                  text-align: left;
                  position: relative;
                  display: flex;
                  flex-direction: column;
                  z-index: 1;
                  justify-content: start;
                  width: 291px;
                  height: 20px;
                  mix-blend-mode: normal;
                  color: rgba(134, 144, 156, 1);
                  font-size: 14px;
                  line-height: 20px;
                  font-weight: 400;
                  opacity: 1;
                  font-family: "HarmonyOSSansSC-Regular";
                  letter-spacing: 0px;
                  white-space: pre-wrap;
                  order: 1;
                  flex-shrink: 0;
                }
              }
            }
          }
          .pc2-bottom-top-item4 {
            position: relative;
            z-index: 1;
            width: unset;
            height: 240px;
            mix-blend-mode: normal;
            align-content: flex-start;
            order: 0;
            flex: 1;
            .img-pc2 {
              position: relative;
              z-index: 1;
              width: 311px;
              height: 180px;
              border-radius: 8px;
              mix-blend-mode: normal;
              display: flex;
              justify-content: center;
              align-items: center;
              overflow: hidden;
              order: 0;
              flex-shrink: 0;
              align-self: stretch;

              display: flex;
              background-size: cover;
              background-position: center;
              background-repeat: no-repeat;
              background-image: url(https://img.jsdesign2.com/assets/img/6556e73686711ace31ea631a.png#25ebe5445751f295b3f2a216b4622814);
              background-size: 311px 180px;
            }
            .text-pc2 {
              position: relative;
              z-index: 2;
              width: unset;
              height: auto;
              mix-blend-mode: normal;
              display: flex;
              flex-direction: column;
              justify-content: flex-start;
              align-items: flex-start;
              gap: 4px;
              order: 1;
              min-height: auto;
              align-self: stretch;
              .text1-pc2 {
                position: relative;
                z-index: 1;
                width: unset;
                height: auto;
                mix-blend-mode: normal;
                display: flex;
                justify-content: flex-start;
                align-items: flex-start;
                overflow: hidden;
                gap: 8px;
                order: 0;
                min-height: auto;
                align-self: stretch;
              }
              .text2-pc2 {
                position: relative;
                z-index: 2;
                width: unset;
                height: auto;
                mix-blend-mode: normal;
                display: flex;
                justify-content: flex-start;
                align-items: center;
                gap: 4px;
                order: 1;
                min-height: auto;
                align-self: stretch;

                .img-And {
                  position: relative;
                  z-index: 0;
                  border: unset !important;
                  box-shadow: unset;
                  width: 16px;
                  height: 16px;
                  mix-blend-mode: normal;
                  display: flex;
                  background-size: 16px 16px;
                  background-image: url(https://img.jsdesign2.com/assets/element/js_7tbA2BbXK7x/image/916727f446e547a123e7761fbe334216331b5ec9.png);
                  order: 0;
                  flex-shrink: 0;
                }
                .img-text {
                  text-align: left;
                  position: relative;
                  display: flex;
                  flex-direction: column;
                  z-index: 1;
                  justify-content: start;
                  width: 291px;
                  height: 20px;
                  mix-blend-mode: normal;
                  color: rgba(134, 144, 156, 1);
                  font-size: 14px;
                  line-height: 20px;
                  font-weight: 400;
                  opacity: 1;
                  font-family: "HarmonyOSSansSC-Regular";
                  letter-spacing: 0px;
                  white-space: pre-wrap;
                  order: 1;
                  flex-shrink: 0;
                }
              }
            }
          }
        }
        .pc2-bottom-bottom {
          left: 50px;
          position: relative;
          z-index: 2;
          width: unset;
          height: auto;
          mix-blend-mode: normal;
          display: flex;
          justify-content: flex-start;
          align-items: flex-start;
          overflow: hidden;
          gap: 12px;
          order: 1;
          min-height: auto;
          align-self: stretch;
          .pc2-bottom-top-item5 {
            position: relative;
            z-index: 1;
            width: unset;
            height: 240px;
            mix-blend-mode: normal;
            align-content: flex-start;
            order: 0;
            flex: 1;
            .img-pc2 {
              position: relative;
              z-index: 1;
              width: 311px;
              height: 180px;
              border-radius: 8px;
              mix-blend-mode: normal;
              display: flex;
              justify-content: center;
              align-items: center;
              overflow: hidden;
              order: 0;
              flex-shrink: 0;
              align-self: stretch;

              display: flex;
              background-size: cover;
              background-position: center;
              background-repeat: no-repeat;
              background-image: url(https://img.jsdesign2.com/assets/img/6556e73686711ace31ea631a.png#25ebe5445751f295b3f2a216b4622814);
              background-size: 311px 180px;
            }
            .text-pc2 {
              position: relative;
              z-index: 2;
              width: unset;
              height: auto;
              mix-blend-mode: normal;
              display: flex;
              flex-direction: column;
              justify-content: flex-start;
              align-items: flex-start;
              gap: 4px;
              order: 1;
              min-height: auto;
              align-self: stretch;
              .text1-pc2 {
                position: relative;
                z-index: 1;
                width: unset;
                height: auto;
                mix-blend-mode: normal;
                display: flex;
                justify-content: flex-start;
                align-items: flex-start;
                overflow: hidden;
                gap: 8px;
                order: 0;
                min-height: auto;
                align-self: stretch;
              }
              .text2-pc2 {
                position: relative;
                z-index: 2;
                width: unset;
                height: auto;
                mix-blend-mode: normal;
                display: flex;
                justify-content: flex-start;
                align-items: center;
                gap: 4px;
                order: 1;
                min-height: auto;
                align-self: stretch;

                .img-And {
                  position: relative;
                  z-index: 0;
                  border: unset !important;
                  box-shadow: unset;
                  width: 16px;
                  height: 16px;
                  mix-blend-mode: normal;
                  display: flex;
                  background-size: 16px 16px;
                  background-image: url(https://img.jsdesign2.com/assets/element/js_7tbA2BbXK7x/image/916727f446e547a123e7761fbe334216331b5ec9.png);
                  order: 0;
                  flex-shrink: 0;
                }
                .img-text {
                  text-align: left;
                  position: relative;
                  display: flex;
                  flex-direction: column;
                  z-index: 1;
                  justify-content: start;
                  width: 291px;
                  height: 20px;
                  mix-blend-mode: normal;
                  color: rgba(134, 144, 156, 1);
                  font-size: 14px;
                  line-height: 20px;
                  font-weight: 400;
                  opacity: 1;
                  font-family: "HarmonyOSSansSC-Regular";
                  letter-spacing: 0px;
                  white-space: pre-wrap;
                  order: 1;
                  flex-shrink: 0;
                }
              }
            }
          }
          .pc2-bottom-top-item6 {
            position: relative;
            z-index: 1;
            width: unset;
            height: 240px;
            mix-blend-mode: normal;
            align-content: flex-start;
            order: 0;
            flex: 1;
            .img-pc2 {
              position: relative;
              z-index: 1;
              width: 311px;
              height: 180px;
              border-radius: 8px;
              mix-blend-mode: normal;
              display: flex;
              justify-content: center;
              align-items: center;
              overflow: hidden;
              order: 0;
              flex-shrink: 0;
              align-self: stretch;

              display: flex;
              background-size: cover;
              background-position: center;
              background-repeat: no-repeat;
              background-image: url(https://img.jsdesign2.com/assets/img/6556e73686711ace31ea631a.png#25ebe5445751f295b3f2a216b4622814);
              background-size: 311px 180px;
            }
            .text-pc2 {
              position: relative;
              z-index: 2;
              width: unset;
              height: auto;
              mix-blend-mode: normal;
              display: flex;
              flex-direction: column;
              justify-content: flex-start;
              align-items: flex-start;
              gap: 4px;
              order: 1;
              min-height: auto;
              align-self: stretch;
              .text1-pc2 {
                position: relative;
                z-index: 1;
                width: unset;
                height: auto;
                mix-blend-mode: normal;
                display: flex;
                justify-content: flex-start;
                align-items: flex-start;
                overflow: hidden;
                gap: 8px;
                order: 0;
                min-height: auto;
                align-self: stretch;
              }
              .text2-pc2 {
                position: relative;
                z-index: 2;
                width: unset;
                height: auto;
                mix-blend-mode: normal;
                display: flex;
                justify-content: flex-start;
                align-items: center;
                gap: 4px;
                order: 1;
                min-height: auto;
                align-self: stretch;

                .img-And {
                  position: relative;
                  z-index: 0;
                  border: unset !important;
                  box-shadow: unset;
                  width: 16px;
                  height: 16px;
                  mix-blend-mode: normal;
                  display: flex;
                  background-position: center;
                  background-repeat: no-repeat;
                  background-size: 16px 16px;
                  background-image: url(https://img.jsdesign2.com/assets/element/js_7tbA2BbXK7x/image/916727f446e547a123e7761fbe334216331b5ec9.png);
                  order: 0;
                  flex-shrink: 0;
                }
                .img-text {
                  text-align: left;
                  position: relative;
                  display: flex;
                  flex-direction: column;
                  z-index: 1;
                  justify-content: start;
                  width: 291px;
                  height: 20px;
                  mix-blend-mode: normal;
                  color: rgba(134, 144, 156, 1);
                  font-size: 14px;
                  line-height: 20px;
                  font-weight: 400;
                  opacity: 1;
                  font-family: "HarmonyOSSansSC-Regular";
                  letter-spacing: 0px;
                  white-space: pre-wrap;
                  order: 1;
                  flex-shrink: 0;
                }
              }
            }
          }
          .pc2-bottom-top-item7 {
            position: relative;
            z-index: 1;
            width: unset;
            height: 240px;
            mix-blend-mode: normal;
            align-content: flex-start;
            order: 0;
            flex: 1;
            .img-pc2 {
              position: relative;
              z-index: 1;
              width: 311px;
              height: 180px;
              border-radius: 8px;
              mix-blend-mode: normal;
              display: flex;
              justify-content: center;
              align-items: center;
              overflow: hidden;
              order: 0;
              flex-shrink: 0;
              align-self: stretch;

              display: flex;
              background-size: cover;
              background-position: center;
              background-repeat: no-repeat;
              background-image: url(https://img.jsdesign2.com/assets/img/6556e73686711ace31ea631a.png#25ebe5445751f295b3f2a216b4622814);
              background-size: 311px 180px;
            }
            .text-pc2 {
              position: relative;
              z-index: 2;
              width: unset;
              height: auto;
              mix-blend-mode: normal;
              display: flex;
              flex-direction: column;
              justify-content: flex-start;
              align-items: flex-start;
              gap: 4px;
              order: 1;
              min-height: auto;
              align-self: stretch;
              .text1-pc2 {
                position: relative;
                z-index: 1;
                width: unset;
                height: auto;
                mix-blend-mode: normal;
                display: flex;
                justify-content: flex-start;
                align-items: flex-start;
                overflow: hidden;
                gap: 8px;
                order: 0;
                min-height: auto;
                align-self: stretch;
              }
              .text2-pc2 {
                position: relative;
                z-index: 2;
                width: unset;
                height: auto;
                mix-blend-mode: normal;
                display: flex;
                justify-content: flex-start;
                align-items: center;
                gap: 4px;
                order: 1;
                min-height: auto;
                align-self: stretch;

                .img-And {
                  position: relative;
                  z-index: 0;
                  border: unset !important;
                  box-shadow: unset;
                  width: 16px;
                  height: 16px;
                  mix-blend-mode: normal;
                  display: flex;
                  background-size: 16px 16px;
                  background-image: url(https://img.jsdesign2.com/assets/element/js_7tbA2BbXK7x/image/916727f446e547a123e7761fbe334216331b5ec9.png);
                  order: 0;
                  flex-shrink: 0;
                }
                .img-text {
                  text-align: left;
                  position: relative;
                  display: flex;
                  flex-direction: column;
                  z-index: 1;
                  justify-content: start;
                  width: 291px;
                  height: 20px;
                  mix-blend-mode: normal;
                  color: rgba(134, 144, 156, 1);
                  font-size: 14px;
                  line-height: 20px;
                  font-weight: 400;
                  opacity: 1;
                  font-family: "HarmonyOSSansSC-Regular";
                  letter-spacing: 0px;
                  white-space: pre-wrap;
                  order: 1;
                  flex-shrink: 0;
                }
              }
            }
          }
          .pc2-bottom-top-item8 {
            position: relative;
            z-index: 1;
            width: unset;
            height: 240px;
            mix-blend-mode: normal;
            align-content: flex-start;
            order: 0;
            flex: 1;
            .img-pc2 {
              position: relative;
              z-index: 1;
              width: 311px;
              height: 180px;
              border-radius: 8px;
              mix-blend-mode: normal;
              display: flex;
              justify-content: center;
              align-items: center;
              overflow: hidden;
              order: 0;
              flex-shrink: 0;
              align-self: stretch;

              display: flex;
              background-size: cover;
              background-position: center;
              background-repeat: no-repeat;
              background-image: url(https://img.jsdesign2.com/assets/img/6556e73686711ace31ea631a.png#25ebe5445751f295b3f2a216b4622814);
              background-size: 311px 180px;
            }
            .text-pc2 {
              position: relative;
              z-index: 2;
              width: unset;
              height: auto;
              mix-blend-mode: normal;
              display: flex;
              flex-direction: column;
              justify-content: flex-start;
              align-items: flex-start;
              gap: 4px;
              order: 1;
              min-height: auto;
              align-self: stretch;
              .text1-pc2 {
                position: relative;
                z-index: 1;
                width: unset;
                height: auto;
                mix-blend-mode: normal;
                display: flex;
                justify-content: flex-start;
                align-items: flex-start;
                overflow: hidden;
                gap: 8px;
                order: 0;
                min-height: auto;
                align-self: stretch;
              }
              .text2-pc2 {
                position: relative;
                z-index: 2;
                width: unset;
                height: auto;
                mix-blend-mode: normal;
                display: flex;
                justify-content: flex-start;
                align-items: center;
                gap: 4px;
                order: 1;
                min-height: auto;
                align-self: stretch;

                .img-And {
                  position: relative;
                  z-index: 0;
                  border: unset !important;
                  box-shadow: unset;
                  width: 16px;
                  height: 16px;
                  mix-blend-mode: normal;
                  display: flex;
                  background-size: 16px 16px;
                  background-image: url(https://img.jsdesign2.com/assets/element/js_7tbA2BbXK7x/image/916727f446e547a123e7761fbe334216331b5ec9.png);
                  flex-shrink: 0;
                  background-size: 16px 16px;
                }
                .img-text {
                  text-align: left;
                  position: relative;
                  display: flex;
                  flex-direction: column;
                  z-index: 1;
                  justify-content: start;
                  width: 291px;
                  height: 20px;
                  mix-blend-mode: normal;
                  color: rgba(134, 144, 156, 1);
                  font-size: 14px;
                  line-height: 20px;
                  font-weight: 400;
                  opacity: 1;
                  font-family: "HarmonyOSSansSC-Regular";
                  letter-spacing: 0px;
                  white-space: pre-wrap;
                  order: 1;
                  flex-shrink: 0;
                }
              }
            }
          }
        }

        // .pc2b-forehead {
        //   position: relative;
        //   z-index: 1;
        //   width: unset;
        //   height: auto;
        //   mix-blend-mode: normal;
        //   display: flex;
        //   justify-content: flex-start;
        //   align-items: flex-start;
        //   overflow: hidden;
        //   gap: 12px;
        //   order: 0;
        //   min-height: auto;
        //   align-self: stretch;
        //   .item1 {
        //     position: relative;
        //     z-index: 1;
        //     width: unset;
        //     height: 240px;
        //     mix-blend-mode: normal;
        //     display: flex;
        //     justify-content: center;
        //     align-items: center;
        //     order: 0;
        //     flex: 1;

        //     .item1-img {
        //       position: relative;
        //       z-index: 0;
        //       width: 311px;
        //       height: 180px;
        //       border-radius: 8px;
        //       mix-blend-mode: normal;
        //       display: flex;
        //       background-size: cover;
        //       background-position: center;
        //       background-repeat: no-repeat;
        //       background-image: url(https://img.jsdesign2.com/assets/img/6556e73686711ace31ea631a.png#25ebe5445751f295b3f2a216b4622814);
        //       order: 0;
        //       flex: 1;
        //     }
        //     .item1-txt {
        //       position: relative;
        //       top: 220px;
        //       left: -310px;
        //       z-index: 2;
        //       width: unset;
        //       height: auto;
        //       mix-blend-mode: normal;
        //       display: flex;
        //       flex-direction: column;
        //       justify-content: flex-start;
        //       align-items: flex-start;
        //       gap: 4px;
        //       order: 1;
        //       min-height: auto;
        //       align-self: stretch;
        //       .it1-txt1 {
        //         position: relative;
        //         z-index: 1;
        //         width: unset;
        //         height: auto;
        //         mix-blend-mode: normal;
        //         display: flex;
        //         justify-content: flex-start;
        //         align-items: flex-start;
        //         overflow: hidden;
        //         gap: 8px;
        //         order: 0;
        //         min-height: auto;
        //         align-self: stretch;
        //         .item1-txt1-1 {
        //           position: relative;
        //           display: flex;
        //           flex-direction: column;
        //           z-index: 0;
        //           justify-content: start;
        //           height: 24px;
        //           mix-blend-mode: normal;
        //           color: rgba(29, 33, 41, 1);
        //           font-size: 16px;
        //           line-height: 24px;
        //           font-weight: 400;
        //           opacity: 1;
        //           font-family: "HarmonyOSSansSC-Regular";
        //           letter-spacing: 0px;
        //           white-space: nowrap;
        //           order: 0;
        //           width: auto;
        //         }
        //         .item1-txt1-2 {
        //           position: relative;
        //           display: flex;
        //           flex-direction: column;
        //           z-index: 1;
        //           justify-content: start;
        //           height: 24px;
        //           mix-blend-mode: normal;
        //           color: rgba(134, 144, 156, 1);
        //           font-size: 16px;
        //           line-height: 24px;
        //           font-weight: 400;
        //           opacity: 1;
        //           font-family: "HarmonyOSSansSC-Regular";
        //           letter-spacing: 0px;
        //           white-space: nowrap;
        //           order: 1;
        //           width: auto;
        //         }
        //       }
        //       .it1-txt2 {
        //         position: relative;
        //         z-index: 2;
        //         width: unset;
        //         height: auto;
        //         mix-blend-mode: normal;
        //         display: flex;
        //         justify-content: flex-start;
        //         align-items: center;
        //         gap: 4px;
        //         order: 1;
        //         min-height: auto;
        //         align-self: stretch;
        //         .item1-txt2-icon {
        //           position: absolute;
        //           top: 0;
        //           left: 0;
        //           right: 0;
        //           bottom: 0;
        //           content: "";
        //           opacity: 1;
        //           background-image: var(--bg-img);
        //           background-size: cover;

        //           position: relative;
        //           z-index: 0;

        //           box-shadow: unset;
        //           width: 16px;
        //           height: 16px;
        //           mix-blend-mode: normal;
        //           display: flex;
        //           background-size: cover;
        //           background-position: center;
        //           background-repeat: no-repeat;
        //           background-image: url(https://img.jsdesign2.com/assets/element/js_gyewIwpzzNH/image/916727f446e547a123e7761fbe334216331b5ec9.png);
        //           order: 0;
        //           flex-shrink: 0;
        //         }
        //         .item1-txt2-2 {
        //           position: relative;
        //           display: flex;
        //           flex-direction: column;
        //           z-index: 1;
        //           justify-content: start;
        //           width: 291px;
        //           height: 20px;
        //           mix-blend-mode: normal;
        //           color: rgba(134, 144, 156, 1);
        //           font-size: 14px;
        //           line-height: 20px;
        //           font-weight: 400;
        //           opacity: 1;
        //           font-family: "HarmonyOSSansSC-Regular";
        //           letter-spacing: 0px;
        //           white-space: pre-wrap;
        //           order: 1;
        //           flex-shrink: 0;
        //         }
        //       }
        //     }
        //   }
        //   .item2 {
        //     position: relative;
        //     z-index: 2;
        //     width: unset;
        //     height: auto;
        //     mix-blend-mode: normal;
        //     display: flex;
        //     flex-direction: column;
        //     justify-content: flex-start;
        //     align-items: flex-start;
        //     gap: 12px;
        //     order: 1;
        //     flex: 1;
        //     .item2-img {
        //       position: relative;
        //       z-index: 0;
        //       width: unset;
        //       height: 180px;
        //       border-radius: 8px;
        //       mix-blend-mode: normal;
        //       display: flex;
        //       background-size: cover;
        //       background-position: center;
        //       background-repeat: no-repeat;
        //       background-image: url(https://img.jsdesign2.com/assets/img/6556e74f43b95387d42669fb.png#6b7a56d0cdc93a4f90696fda6ce1b4f8);
        //       order: 0;
        //       flex: 1;
        //     }
        //     .item2-txt {
        //       position: relative;

        //       z-index: 2;
        //       width: unset;
        //       height: auto;
        //       mix-blend-mode: normal;
        //       display: flex;
        //       flex-direction: column;
        //       justify-content: flex-start;
        //       align-items: flex-start;
        //       gap: 4px;
        //       order: 1;
        //       min-height: auto;
        //       align-self: stretch;
        //       .it2-txt1 {
        //         position: relative;
        //         z-index: 1;
        //         width: unset;
        //         height: auto;
        //         mix-blend-mode: normal;
        //         display: flex;
        //         justify-content: flex-start;
        //         align-items: flex-start;
        //         gap: 8px;
        //         order: 0;
        //         min-height: auto;
        //         align-self: stretch;
        //         .item2-txt1-1 {
        //           position: relative;
        //           display: flex;
        //           flex-direction: column;
        //           z-index: 0;
        //           justify-content: start;
        //           height: 24px;
        //           mix-blend-mode: normal;
        //           color: rgba(29, 33, 41, 1);
        //           font-size: 16px;
        //           line-height: 24px;
        //           font-weight: 400;
        //           opacity: 1;
        //           font-family: "HarmonyOSSansSC-Regular";
        //           letter-spacing: 0px;
        //           white-space: nowrap;
        //           order: 0;
        //           width: auto;
        //         }
        //         .item2-txt1-2 {
        //           position: relative;
        //           display: flex;
        //           flex-direction: column;
        //           z-index: 1;
        //           justify-content: start;
        //           height: 24px;
        //           mix-blend-mode: normal;
        //           color: rgba(134, 144, 156, 1);
        //           font-size: 16px;
        //           line-height: 24px;
        //           font-weight: 400;
        //           opacity: 1;
        //           font-family: "HarmonyOSSansSC-Regular";
        //           letter-spacing: 0px;
        //           white-space: nowrap;
        //           order: 1;
        //           width: auto;
        //         }
        //       }
        //       .it2-txt2 {
        //         position: relative;
        //         z-index: 2;
        //         width: unset;
        //         height: auto;
        //         mix-blend-mode: normal;
        //         display: flex;
        //         justify-content: flex-start;
        //         align-items: center;
        //         gap: 4px;
        //         order: 1;
        //         min-height: auto;
        //         align-self: stretch;
        //         .item2-txt1-icon {
        //           position: relative;
        //           z-index: 0;
        //           border: unset !important;
        //           box-shadow: unset;
        //           width: 16px;
        //           height: 16px;
        //           mix-blend-mode: normal;
        //           display: flex;
        //           background-size: cover;
        //           background-position: center;
        //           background-repeat: no-repeat;
        //           background-image: url(https://img.jsdesign2.com/assets/element/js_gyewIwpzzNH/image/916727f446e547a123e7761fbe334216331b5ec9.png);
        //           order: 0;
        //           flex-shrink: 0;
        //         }
        //         .item2-txt2-2 {
        //           position: relative;
        //           display: flex;
        //           flex-direction: column;
        //           z-index: 1;
        //           justify-content: start;
        //           width: 291px;
        //           height: 20px;
        //           mix-blend-mode: normal;
        //           color: rgba(134, 144, 156, 1);
        //           font-size: 14px;
        //           line-height: 20px;
        //           font-weight: 400;
        //           opacity: 1;
        //           font-family: "HarmonyOSSansSC-Regular";
        //           letter-spacing: 0px;
        //           white-space: pre-wrap;
        //           order: 1;
        //           flex-shrink: 0;
        //         }
        //       }
        //     }
        //   }
        //   .item3 {
        //     position: relative;
        //     z-index: 3;
        //     width: unset;
        //     height: auto;
        //     mix-blend-mode: normal;
        //     display: flex;
        //     flex-direction: column;
        //     justify-content: flex-start;
        //     align-items: flex-start;
        //     gap: 12px;
        //     order: 2;
        //     flex: 1;
        //     .item3-img {
        //       position: relative;
        //       z-index: 0;
        //       width: unset;
        //       height: 180px;
        //       border-radius: 8px;
        //       mix-blend-mode: normal;
        //       display: flex;
        //       background-size: cover;
        //       background-position: center;
        //       background-repeat: no-repeat;
        //       background-image: url(https://img.jsdesign2.com/assets/img/6556e74f86711ace31ea63ab.png#153a273c83b681d3992638ddce7d636e);
        //       order: 0;
        //       flex: 1;
        //     }
        //     .item3-txt {
        //       position: relative;
        //       z-index: 2;
        //       width: unset;
        //       height: auto;
        //       mix-blend-mode: normal;
        //       display: flex;
        //       flex-direction: column;
        //       justify-content: flex-start;
        //       align-items: flex-start;
        //       gap: 4px;
        //       order: 1;
        //       min-height: auto;
        //       align-self: stretch;
        //       .it3-txt1 {
        //         position: relative;
        //         z-index: 1;
        //         width: unset;
        //         height: auto;
        //         mix-blend-mode: normal;
        //         display: flex;
        //         justify-content: flex-start;
        //         align-items: flex-start;
        //         gap: 8px;
        //         order: 0;
        //         min-height: auto;
        //         align-self: stretch;
        //         .item3-txt1-1 {
        //           position: relative;
        //           display: flex;
        //           flex-direction: column;
        //           z-index: 0;
        //           justify-content: start;
        //           height: 24px;
        //           mix-blend-mode: normal;
        //           color: rgba(29, 33, 41, 1);
        //           font-size: 16px;
        //           line-height: 24px;
        //           font-weight: 400;
        //           opacity: 1;
        //           font-family: "HarmonyOSSansSC-Regular";
        //           letter-spacing: 0px;
        //           white-space: nowrap;
        //           order: 0;
        //           width: auto;
        //         }
        //         .item3-txt1-2 {
        //           position: relative;
        //           display: flex;
        //           flex-direction: column;
        //           z-index: 1;
        //           justify-content: start;
        //           height: 24px;
        //           mix-blend-mode: normal;
        //           color: rgba(134, 144, 156, 1);
        //           font-size: 16px;
        //           line-height: 24px;
        //           font-weight: 400;
        //           opacity: 1;
        //           font-family: "HarmonyOSSansSC-Regular";
        //           letter-spacing: 0px;
        //           white-space: nowrap;
        //           order: 1;
        //           width: auto;
        //         }
        //       }
        //       .it3-txt2 {
        //         position: relative;
        //         z-index: 2;
        //         width: unset;
        //         height: auto;
        //         mix-blend-mode: normal;
        //         display: flex;
        //         justify-content: flex-start;
        //         align-items: center;
        //         gap: 4px;
        //         order: 1;
        //         min-height: auto;
        //         align-self: stretch;
        //         .item3-txt1-icon {
        //           position: relative;
        //           z-index: 0;
        //           border: unset !important;
        //           box-shadow: unset;
        //           width: 16px;
        //           height: 16px;
        //           mix-blend-mode: normal;
        //           display: flex;
        //           background-size: cover;
        //           background-position: center;
        //           background-repeat: no-repeat;
        //           background-image: url(https://img.jsdesign2.com/assets/element/js_gyewIwpzzNH/image/916727f446e547a123e7761fbe334216331b5ec9.png);
        //           order: 0;
        //           flex-shrink: 0;
        //         }
        //         .item3-txt2-2 {
        //           position: relative;
        //           display: flex;
        //           flex-direction: column;
        //           z-index: 1;
        //           justify-content: start;
        //           width: 291px;
        //           height: 20px;
        //           mix-blend-mode: normal;
        //           color: rgba(134, 144, 156, 1);
        //           font-size: 14px;
        //           line-height: 20px;
        //           font-weight: 400;
        //           opacity: 1;
        //           font-family: "HarmonyOSSansSC-Regular";
        //           letter-spacing: 0px;
        //           white-space: pre-wrap;
        //           order: 1;
        //           flex-shrink: 0;
        //         }
        //       }
        //     }
        //   }
        //   .item4 {
        //     position: relative;
        //     z-index: 4;
        //     width: unset;
        //     height: auto;
        //     mix-blend-mode: normal;
        //     display: flex;
        //     flex-direction: column;
        //     justify-content: flex-start;
        //     align-items: flex-start;
        //     gap: 12px;
        //     order: 3;
        //     flex: 1;
        //     .item4-img {
        //       position: relative;
        //       z-index: 0;
        //       width: unset;
        //       height: 180px;
        //       border-radius: 8px;
        //       mix-blend-mode: normal;
        //       display: flex;
        //       background-size: cover;
        //       background-position: center;
        //       background-repeat: no-repeat;
        //       background-image: url(https://img.jsdesign2.com/assets/img/6556e73fe1e45fa4efce1420.png#af9528f906d97ad9c68164f4572a6ec4);
        //       order: 0;
        //       flex: 1;
        //     }
        //     .item4-txt {
        //       position: relative;
        //       z-index: 2;
        //       width: unset;
        //       height: auto;
        //       mix-blend-mode: normal;
        //       display: flex;
        //       flex-direction: column;
        //       justify-content: flex-start;
        //       align-items: flex-start;
        //       gap: 4px;
        //       order: 1;
        //       min-height: auto;
        //       align-self: stretch;
        //       .it4-txt1 {
        //         position: relative;
        //         z-index: 1;
        //         width: unset;
        //         height: auto;
        //         mix-blend-mode: normal;
        //         display: flex;
        //         justify-content: flex-start;
        //         align-items: flex-start;
        //         gap: 8px;
        //         order: 0;
        //         min-height: auto;
        //         align-self: stretch;
        //         .item4-txt1-1 {
        //           position: relative;
        //           display: flex;
        //           flex-direction: column;
        //           z-index: 0;
        //           justify-content: start;
        //           height: 24px;
        //           mix-blend-mode: normal;
        //           color: rgba(29, 33, 41, 1);
        //           font-size: 16px;
        //           line-height: 24px;
        //           font-weight: 400;
        //           opacity: 1;
        //           font-family: "HarmonyOSSansSC-Regular";
        //           letter-spacing: 0px;
        //           white-space: nowrap;
        //           order: 0;
        //           width: auto;
        //         }
        //         .item4-txt1-2 {
        //           position: relative;
        //           display: flex;
        //           flex-direction: column;
        //           z-index: 1;
        //           justify-content: start;
        //           height: 24px;
        //           mix-blend-mode: normal;
        //           color: rgba(134, 144, 156, 1);
        //           font-size: 16px;
        //           line-height: 24px;
        //           font-weight: 400;
        //           opacity: 1;
        //           font-family: "HarmonyOSSansSC-Regular";
        //           letter-spacing: 0px;
        //           white-space: nowrap;
        //           order: 1;
        //           width: auto;
        //         }
        //       }
        //       .it4-txt2 {
        //         position: relative;
        //         z-index: 2;
        //         width: unset;
        //         height: auto;
        //         mix-blend-mode: normal;
        //         display: flex;
        //         justify-content: flex-start;
        //         align-items: center;
        //         gap: 4px;
        //         order: 1;
        //         min-height: auto;
        //         align-self: stretch;
        //         .item4-txt1-icon {
        //           position: relative;
        //           z-index: 0;
        //           border: unset !important;
        //           box-shadow: unset;
        //           width: 16px;
        //           height: 16px;
        //           mix-blend-mode: normal;
        //           display: flex;
        //           background-size: cover;
        //           background-position: center;
        //           background-repeat: no-repeat;
        //           background-image: url(https://img.jsdesign2.com/assets/element/js_gyewIwpzzNH/image/916727f446e547a123e7761fbe334216331b5ec9.png);
        //           order: 0;
        //           flex-shrink: 0;
        //         }
        //         .item4-txt2-2 {
        //           position: relative;
        //           display: flex;
        //           flex-direction: column;
        //           z-index: 1;
        //           justify-content: start;
        //           width: 291px;
        //           height: 20px;
        //           mix-blend-mode: normal;
        //           color: rgba(134, 144, 156, 1);
        //           font-size: 14px;
        //           line-height: 20px;
        //           font-weight: 400;
        //           opacity: 1;
        //           font-family: "HarmonyOSSansSC-Regular";
        //           letter-spacing: 0px;
        //           white-space: pre-wrap;
        //           order: 1;
        //           flex-shrink: 0;
        //         }
        //       }
        //     }
        //   }
        // }
        // .pc2b-bottom {
        //   position: relative;
        //   z-index: 2;
        //   width: unset;
        //   height: auto;
        //   mix-blend-mode: normal;
        //   display: flex;
        //   justify-content: flex-start;
        //   align-items: flex-start;
        //   overflow: hidden;
        //   gap: 12px;
        //   order: 1;
        //   min-height: auto;
        //   align-self: stretch;
        //   .item5 {
        //     position: relative;
        //     z-index: 1;
        //     width: unset;
        //     height: auto;
        //     mix-blend-mode: normal;
        //     display: flex;
        //     flex-direction: column;
        //     justify-content: flex-start;
        //     align-items: flex-start;
        //     gap: 12px;
        //     order: 0;
        //     flex: 1;
        //     .item5-img {
        //       position: relative;
        //       z-index: 0;
        //       width: unset;
        //       height: 180px;
        //       border-radius: 8px;
        //       mix-blend-mode: normal;
        //       display: flex;
        //       background-size: cover;
        //       background-position: center;
        //       background-repeat: no-repeat;
        //       background-image: url(https://img.jsdesign2.com/assets/img/657561a3c464574bd9b35a0b.png#0270437425b77b8ddb07ceeab65ba732);
        //       order: 0;
        //       flex: 1;
        //     }
        //     .item5-txt {
        //       position: relative;
        //       z-index: 2;
        //       width: unset;
        //       height: auto;
        //       mix-blend-mode: normal;
        //       display: flex;
        //       flex-direction: column;
        //       justify-content: flex-start;
        //       align-items: flex-start;
        //       gap: 4px;
        //       order: 1;
        //       min-height: auto;
        //       align-self: stretch;
        //       .it5-txt1 {
        //         position: relative;
        //         z-index: 1;
        //         width: unset;
        //         height: auto;
        //         mix-blend-mode: normal;
        //         display: flex;
        //         justify-content: flex-start;
        //         align-items: flex-start;
        //         gap: 8px;
        //         order: 0;
        //         min-height: auto;
        //         align-self: stretch;
        //         .item5-txt1-1 {
        //           position: relative;
        //           display: flex;
        //           flex-direction: column;
        //           z-index: 0;
        //           justify-content: start;
        //           height: 24px;
        //           mix-blend-mode: normal;
        //           color: rgba(29, 33, 41, 1);
        //           font-size: 16px;
        //           line-height: 24px;
        //           font-weight: 400;
        //           opacity: 1;
        //           font-family: "HarmonyOSSansSC-Regular";
        //           letter-spacing: 0px;
        //           white-space: nowrap;
        //           order: 0;
        //           width: auto;
        //         }
        //         .item5-txt1-2 {
        //           position: relative;
        //           display: flex;
        //           flex-direction: column;
        //           z-index: 1;
        //           justify-content: start;
        //           height: 24px;
        //           mix-blend-mode: normal;
        //           color: rgba(134, 144, 156, 1);
        //           font-size: 16px;
        //           line-height: 24px;
        //           font-weight: 400;
        //           opacity: 1;
        //           font-family: "HarmonyOSSansSC-Regular";
        //           letter-spacing: 0px;
        //           white-space: nowrap;
        //           order: 1;
        //           width: auto;
        //         }
        //       }
        //       .it5-txt2 {
        //         position: relative;
        //         z-index: 2;
        //         width: auto;
        //         height: auto;
        //         mix-blend-mode: normal;
        //         display: flex;
        //         justify-content: flex-start;
        //         align-items: center;
        //         gap: 4px;
        //         order: 1;
        //         min-height: auto;
        //         .item5-txt1-icon {
        //           position: relative;
        //           z-index: 0;
        //           border: unset !important;
        //           box-shadow: unset;
        //           width: 16px;
        //           height: 16px;
        //           mix-blend-mode: normal;
        //           display: flex;
        //           background-size: cover;
        //           background-position: center;
        //           background-repeat: no-repeat;
        //           background-image: url(https://img.jsdesign2.com/assets/element/js_gyewIwpzzNH/image/916727f446e547a123e7761fbe334216331b5ec9.png);
        //           order: 0;
        //           flex-shrink: 0;
        //         }
        //         .item5-txt2-2 {
        //           position: relative;
        //           display: flex;
        //           flex-direction: column;
        //           z-index: 1;
        //           justify-content: start;
        //           height: 20px;
        //           mix-blend-mode: normal;
        //           color: rgba(134, 144, 156, 1);
        //           font-size: 14px;
        //           line-height: 20px;
        //           font-weight: 400;
        //           opacity: 1;
        //           font-family: "HarmonyOSSansSC-Regular";
        //           letter-spacing: 0px;
        //           white-space: nowrap;
        //           order: 1;
        //           width: auto;
        //         }
        //       }
        //     }
        //   }
        //   .item6 {
        //     position: relative;
        //     z-index: 2;
        //     width: unset;
        //     height: auto;
        //     mix-blend-mode: normal;
        //     display: flex;
        //     flex-direction: column;
        //     justify-content: flex-start;
        //     align-items: flex-start;
        //     gap: 12px;
        //     order: 1;
        //     flex: 1;
        //     .item6-img {
        //       position: relative;
        //       z-index: 0;
        //       width: unset;
        //       height: 180px;
        //       border-radius: 8px;
        //       mix-blend-mode: normal;
        //       display: flex;
        //       background-size: cover;
        //       background-position: center;
        //       background-repeat: no-repeat;
        //       background-image: url(https://img.jsdesign2.com/assets/img/6556e74fe739773bfac4bbbf.png#2687924da7bf308d5680d8c5b1d44fff);
        //       order: 0;
        //       flex: 1;
        //     }
        //     .item6-txt {
        //       position: relative;
        //       z-index: 2;
        //       width: unset;
        //       height: auto;
        //       mix-blend-mode: normal;
        //       display: flex;
        //       flex-direction: column;
        //       justify-content: flex-start;
        //       align-items: flex-start;
        //       gap: 4px;
        //       order: 1;
        //       min-height: auto;
        //       align-self: stretch;
        //       .it6-txt1 {
        //         position: relative;
        //         z-index: 1;
        //         width: unset;
        //         height: auto;
        //         mix-blend-mode: normal;
        //         display: flex;
        //         justify-content: flex-start;
        //         align-items: flex-start;
        //         gap: 8px;
        //         order: 0;
        //         min-height: auto;
        //         align-self: stretch;
        //         .item6-txt1-1 {
        //           position: relative;
        //           display: flex;
        //           flex-direction: column;
        //           z-index: 0;
        //           justify-content: start;
        //           height: 24px;
        //           mix-blend-mode: normal;
        //           color: rgba(29, 33, 41, 1);
        //           font-size: 16px;
        //           line-height: 24px;
        //           font-weight: 400;
        //           opacity: 1;
        //           font-family: "HarmonyOSSansSC-Regular";
        //           letter-spacing: 0px;
        //           white-space: nowrap;
        //           order: 0;
        //           width: auto;
        //         }
        //         .item6-txt1-2 {
        //           position: relative;
        //           display: flex;
        //           flex-direction: column;
        //           z-index: 1;
        //           justify-content: start;
        //           height: 24px;
        //           mix-blend-mode: normal;
        //           color: rgba(134, 144, 156, 1);
        //           font-size: 16px;
        //           line-height: 24px;
        //           font-weight: 400;
        //           opacity: 1;
        //           font-family: "HarmonyOSSansSC-Regular";
        //           letter-spacing: 0px;
        //           white-space: nowrap;
        //           order: 1;
        //           width: auto;
        //         }
        //       }
        //       .it6-txt2 {
        //         position: relative;
        //         z-index: 2;
        //         width: auto;
        //         height: auto;
        //         mix-blend-mode: normal;
        //         display: flex;
        //         justify-content: flex-start;
        //         align-items: center;
        //         gap: 4px;
        //         order: 1;
        //         min-height: auto;
        //         .item6-txt1-icon {
        //           position: relative;
        //           z-index: 0;
        //           border: unset !important;
        //           box-shadow: unset;
        //           width: 16px;
        //           height: 16px;
        //           mix-blend-mode: normal;
        //           display: flex;
        //           background-size: cover;
        //           background-position: center;
        //           background-repeat: no-repeat;
        //           background-image: url(https://img.jsdesign2.com/assets/element/js_gyewIwpzzNH/image/916727f446e547a123e7761fbe334216331b5ec9.png);
        //           order: 0;
        //           flex-shrink: 0;
        //         }
        //         .item6-txt2-2 {
        //           position: relative;
        //           display: flex;
        //           flex-direction: column;
        //           z-index: 1;
        //           justify-content: start;
        //           height: 20px;
        //           mix-blend-mode: normal;
        //           color: rgba(134, 144, 156, 1);
        //           font-size: 14px;
        //           line-height: 20px;
        //           font-weight: 400;
        //           opacity: 1;
        //           font-family: "HarmonyOSSansSC-Regular";
        //           letter-spacing: 0px;
        //           white-space: nowrap;
        //           order: 1;
        //           width: auto;
        //         }
        //       }
        //     }
        //   }
        //   .item7 {
        //     position: relative;
        //     z-index: 3;
        //     width: unset;
        //     height: auto;
        //     mix-blend-mode: normal;
        //     display: flex;
        //     flex-direction: column;
        //     justify-content: flex-start;
        //     align-items: flex-start;
        //     gap: 12px;
        //     order: 2;
        //     flex: 1;
        //     .item7-img {
        //       position: relative;
        //       z-index: 0;
        //       width: unset;
        //       height: 180px;
        //       border-radius: 8px;
        //       mix-blend-mode: normal;
        //       display: flex;
        //       background-size: cover;
        //       background-position: center;
        //       background-repeat: no-repeat;
        //       background-image: url(https://img.jsdesign2.com/assets/img/6556e73f90ab84325baa606a.png#85d85dbadb9db0744eaa6c894d882c4d);
        //       order: 0;
        //       flex: 1;
        //     }
        //     .item7-txt {
        //       position: relative;
        //       z-index: 2;
        //       width: unset;
        //       height: auto;
        //       mix-blend-mode: normal;
        //       display: flex;
        //       flex-direction: column;
        //       justify-content: flex-start;
        //       align-items: flex-start;
        //       gap: 4px;
        //       order: 1;
        //       min-height: auto;
        //       align-self: stretch;
        //       .it7-txt1 {
        //         position: relative;
        //         z-index: 1;
        //         width: unset;
        //         height: auto;
        //         mix-blend-mode: normal;
        //         display: flex;
        //         justify-content: flex-start;
        //         align-items: flex-start;
        //         gap: 8px;
        //         order: 0;
        //         min-height: auto;
        //         align-self: stretch;
        //         .item7-txt1-1 {
        //           position: relative;
        //           display: flex;
        //           flex-direction: column;
        //           z-index: 0;
        //           justify-content: start;
        //           height: 24px;
        //           mix-blend-mode: normal;
        //           color: rgba(29, 33, 41, 1);
        //           font-size: 16px;
        //           line-height: 24px;
        //           font-weight: 400;
        //           opacity: 1;
        //           font-family: "HarmonyOSSansSC-Regular";
        //           letter-spacing: 0px;
        //           white-space: nowrap;
        //           order: 0;
        //           width: auto;
        //         }
        //         .item7-txt1-2 {
        //           position: relative;
        //           display: flex;
        //           flex-direction: column;
        //           z-index: 1;
        //           justify-content: start;
        //           height: 24px;
        //           mix-blend-mode: normal;
        //           color: rgba(134, 144, 156, 1);
        //           font-size: 16px;
        //           line-height: 24px;
        //           font-weight: 400;
        //           opacity: 1;
        //           font-family: "HarmonyOSSansSC-Regular";
        //           letter-spacing: 0px;
        //           white-space: nowrap;
        //           order: 1;
        //           width: auto;
        //         }
        //       }
        //       .it7-txt2 {
        //         position: relative;
        //         z-index: 2;
        //         width: auto;
        //         height: auto;
        //         mix-blend-mode: normal;
        //         display: flex;
        //         justify-content: flex-start;
        //         align-items: center;
        //         gap: 4px;
        //         order: 1;
        //         min-height: auto;
        //         .item7-txt1-icon {
        //           position: relative;
        //           z-index: 0;
        //           border: unset !important;
        //           box-shadow: unset;
        //           width: 16px;
        //           height: 16px;
        //           mix-blend-mode: normal;
        //           display: flex;
        //           background-size: cover;
        //           background-position: center;
        //           background-repeat: no-repeat;
        //           background-image: url(https://img.jsdesign2.com/assets/element/js_gyewIwpzzNH/image/916727f446e547a123e7761fbe334216331b5ec9.png);
        //           order: 0;
        //           flex-shrink: 0;
        //         }
        //         .item7-txt2-2 {
        //           position: relative;
        //           display: flex;
        //           flex-direction: column;
        //           z-index: 1;
        //           justify-content: start;
        //           height: 20px;
        //           mix-blend-mode: normal;
        //           color: rgba(134, 144, 156, 1);
        //           font-size: 14px;
        //           line-height: 20px;
        //           font-weight: 400;
        //           opacity: 1;
        //           font-family: "HarmonyOSSansSC-Regular";
        //           letter-spacing: 0px;
        //           white-space: nowrap;
        //           order: 1;
        //           width: auto;
        //         }
        //       }
        //     }
        //   }
        //   .item8 {
        //     position: relative;
        //     z-index: 4;
        //     width: unset;
        //     height: auto;
        //     mix-blend-mode: normal;
        //     display: flex;
        //     flex-direction: column;
        //     justify-content: flex-start;
        //     align-items: flex-start;
        //     gap: 12px;
        //     order: 3;
        //     flex: 1;
        //     .item8-img {
        //       position: relative;
        //       z-index: 0;
        //       width: unset;
        //       height: 180px;
        //       border-radius: 8px;
        //       mix-blend-mode: normal;
        //       display: flex;
        //       background-size: cover;
        //       background-position: center;
        //       background-repeat: no-repeat;
        //       background-image: url(https://img.jsdesign2.com/assets/img/6556e74fe739773bfac4bbbf.png#2687924da7bf308d5680d8c5b1d44fff);
        //       order: 0;
        //       flex: 1;
        //     }
        //     .item8-txt {
        //       position: relative;
        //       z-index: 2;
        //       width: unset;
        //       height: auto;
        //       mix-blend-mode: normal;
        //       display: flex;
        //       flex-direction: column;
        //       justify-content: flex-start;
        //       align-items: flex-start;
        //       gap: 4px;
        //       order: 1;
        //       min-height: auto;
        //       align-self: stretch;
        //       .it8-txt1 {
        //         position: relative;
        //         z-index: 1;
        //         width: unset;
        //         height: auto;
        //         mix-blend-mode: normal;
        //         display: flex;
        //         justify-content: flex-start;
        //         align-items: flex-start;
        //         gap: 8px;
        //         order: 0;
        //         min-height: auto;
        //         align-self: stretch;
        //         .item8-txt1-1 {
        //           position: relative;
        //           display: flex;
        //           flex-direction: column;
        //           z-index: 0;
        //           justify-content: start;
        //           height: 24px;
        //           mix-blend-mode: normal;
        //           color: rgba(29, 33, 41, 1);
        //           font-size: 16px;
        //           line-height: 24px;
        //           font-weight: 400;
        //           opacity: 1;
        //           font-family: "HarmonyOSSansSC-Regular";
        //           letter-spacing: 0px;
        //           white-space: nowrap;
        //           order: 0;
        //           width: auto;
        //         }
        //         .item8-txt1-2 {
        //           position: relative;
        //           display: flex;
        //           flex-direction: column;
        //           z-index: 1;
        //           justify-content: start;
        //           height: 24px;
        //           mix-blend-mode: normal;
        //           color: rgba(134, 144, 156, 1);
        //           font-size: 16px;
        //           line-height: 24px;
        //           font-weight: 400;
        //           opacity: 1;
        //           font-family: "HarmonyOSSansSC-Regular";
        //           letter-spacing: 0px;
        //           white-space: nowrap;
        //           order: 1;
        //           width: auto;
        //         }
        //       }
        //       .it8-txt2 {
        //         position: relative;
        //         z-index: 2;
        //         width: auto;
        //         height: auto;
        //         mix-blend-mode: normal;
        //         display: flex;
        //         justify-content: flex-start;
        //         align-items: center;
        //         gap: 4px;
        //         order: 1;
        //         min-height: auto;
        //         .item8-txt1-icon {
        //           position: relative;
        //           z-index: 0;
        //           border: unset !important;
        //           box-shadow: unset;
        //           width: 16px;
        //           height: 16px;
        //           mix-blend-mode: normal;
        //           display: flex;
        //           background-size: cover;
        //           background-position: center;
        //           background-repeat: no-repeat;
        //           background-image: url(https://img.jsdesign2.com/assets/element/js_gyewIwpzzNH/image/916727f446e547a123e7761fbe334216331b5ec9.png);
        //           order: 0;
        //           flex-shrink: 0;
        //         }
        //         .item8-txt2-2 {
        //           position: relative;
        //           display: flex;
        //           flex-direction: column;
        //           z-index: 1;
        //           justify-content: start;
        //           height: 20px;
        //           mix-blend-mode: normal;
        //           color: rgba(134, 144, 156, 1);
        //           font-size: 14px;
        //           line-height: 20px;
        //           font-weight: 400;
        //           opacity: 1;
        //           font-family: "HarmonyOSSansSC-Regular";
        //           letter-spacing: 0px;
        //           white-space: nowrap;
        //           order: 1;
        //           width: auto;
        //         }
        //       }
        //     }
        //   }
        // }
      }
    }
  }
}
.main-part-3 {
  position: relative;
  z-index: 4;
  width: 100%;
  max-width: 1200px;
  margin: 0 auto;
  /* 设置最小宽度 */
  max-width: 1200px;
  mix-blend-mode: normal;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: center;
  padding: 80px 80px 80px 80px;
  overflow: hidden;
  box-sizing: border-box;
  gap: 80px;
  order: 3;
  min-height: auto;
  align-self: stretch;
  .part3-left {
    position: relative;
    top: 300px;
    left: -440px;

    z-index: 1;
    width: 720px;
    height: 228px;
    mix-blend-mode: normal;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: flex-start;
    gap: 24px;
    order: 0;
    flex: 1;

    .p3l-forehead {
      position: relative;
      top: 130px;
      left: 202px;
      text-align: left;
      display: flex;
      flex-direction: column;
      z-index: 0;
      justify-content: start;
      width: unset;
      mix-blend-mode: normal;
      color: rgba(29, 33, 41, 1);
      font-size: 48px;
      line-height: 56px;
      font-weight: 700;
      opacity: 1;
      font-family: "HarmonyOSSansSC-Bold";
      letter-spacing: 0px;
      white-space: pre-wrap;
      order: 0;
      height: auto;
      align-self: stretch;
    }
    .p3l-center {
      //   display: -webkit-box; /* 必须使用这个显示方式 */
      // -webkit-box-orient: vertical; /* 设置为垂直布局 */
      // -webkit-line-clamp: 5; /* 限制显示为五行 */
      width: 500px;
      position: relative;
      text-align: left;
      left: 206px;
      top: 120px;
      display: flex;
      flex-direction: column;
      z-index: 1;
      justify-content: start;

      mix-blend-mode: normal;
      color: rgba(29, 33, 41, 1);
      font-size: 18px;
      line-height: 28px;
      font-weight: 400;
      opacity: 1;
      font-family: "HarmonyOSSansSC-Regular";
      letter-spacing: 0px;
      // white-space: pre-wrap;
      order: 1;
      height: auto;
      align-self: stretch;
    }
    .p3l-bottom {
      top: 150px;
      position: relative;
      .p3lb-box {
        top: 230px;
        border: solid 1px black;
        left: 210px;
        position: relative;
        z-index: 3;
        width: auto;
        height: auto;
        box-shadow: 4px 4px 0px rgba(0, 0, 0, 1);
        border-radius: 4px;
        mix-blend-mode: normal;
        display: flex;
        justify-content: center;
        align-items: center;
        padding: 8px 20px 8px 20px;
        opacity: 1;
        background: rgba(255, 255, 255, 1);
        box-sizing: border-box;
        gap: 8px;
        order: 2;
        min-height: auto;
        .box-txt {
          color: rgba(29, 33, 41, 1);
          font-size: 16px;
          line-height: 24px;
          font-weight: 400;
          font-family: "HarmonyOSSansSC-Regular";
          letter-spacing: 0px;
          white-space: nowrap;
        }
        .p3lb-icon {
          position: relative;
          z-index: 1;
          border: unset !important;
          box-shadow: unset;
          width: 7.5px;
          height: 12px;
          mix-blend-mode: normal;
          display: flex;
          background-size: cover;
          background-position: center;
          background-repeat: no-repeat;

          background-image: url(https://img.jsdesign2.com/assets/element/js_gyewIwpzzNH/image/b0a0e0d6fb4e27ed7644f67cf1e0aa89e0dae274.png);
          order: 1;
          flex-shrink: 0;
        }
      }
    }
  }
  .part3-right {
    position: relative;
    top: -60px;
    left: 388px;
    width: 720px;
    height: 640px;
    margin-right: 20px;
    background-image: url(https://img.jsdesign2.com/assets/img/6556e74fe739773bfac4bbbf.png);
    background-size: cover; /* 确保图片覆盖整个容器 */
    background-position: center; /* 图片居中 */
    background-repeat: no-repeat; /* 防止背景图片重复 */
  }
}

/*Main样式结束*/
/* footer样式开始 */
.wrap {
  width: 1200px;
  max-width: 1200px;
  /* 设置最小宽度 */
  max-width: 1200px;
  margin: 0 auto;
  .footer {
    position: relative;
    z-index: 5;
    width: unset;
    height: auto;
    mix-blend-mode: normal;
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    align-items: center;
    padding: 80px 80px 80px 80px;
    overflow: hidden;
    box-sizing: border-box;
    gap: 60px;
    order: 4;
    min-height: auto;
    align-self: stretch;
    .footer-forehead {
      position: relative;
      z-index: 1;
      width: unset;
      height: auto;
      mix-blend-mode: normal;
      display: flex;
      justify-content: flex-start;
      align-items: flex-start;
      gap: 120px;
      order: 0;
      min-height: auto;
      align-self: stretch;
      --cursor-pointer: -webkit-image-set(url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAEAAAABACAYAAAHdbkFIAAAAAXNSR0IArs4c6QAAClpJREFUeAHtm2toVdkVx8+9eTpJjIl5GqtmMtTY2sYpRaehKFb8EBEfRacODVgsDi3S+TTS2n7rl9IWi5SOVEpttQ6WQgtSBaGdig+siEIUHyRYOh2MmMT4TGKe9/T/O5N9c+7Jufeec3Mn6dC7YHH23WfvtdZee6291177XMvKJkRtgQhG3ESjrh9OuaamJlZRUfFNb8MIvd2gBp+hs6FgRyKRNipcMEE5gZ9+7ywsLPzc6Ojof1Q+LowJZw00PLu4uHiDl6EZhVO/efPmv9OwqqqqLKGhFPOzbdu2xdXQ3t6ORhOgYMuWLfEGUDFv3XqokQ6+wwvp4X09/mUazc3zldra2pdiXZwJ+3wGCWhMO0UgPwyRUjobAnG1qXDv3j17+fLlaG++m2DCROnFYl729PS42zjlpqYmq6WlhXLFtJeeirKCgoLvHjx40C2APTg4aJeUlPxUbUvd7d3z6K6nXCh8RWjajKg8LJxVGxe/TyVEZQcdlZWVrZLeO82BBlTH/GFMap3ouD7d/Ti4OzHnZhp9uqcRsaur64EkiSGN8MeiUOBLZbIyKg98pIa3GML4+DgPB/bv3+88FyxY8D219ZPaIVG+cuXKyS7+Dyn2pFomeKeb2sjdu3e/NTyMtfqDyI75v5mqXaQh9Pvzt+28vLzNapo31Xx6CYleR2leoE7vVgkTZiXhxyQ9NE3DL2tFqqFOq+xjPTqFl4RDwjj4EeAlkswT4tIAexkdx/mRg/8tDSSbRD8paWsMH5My6Nc2q3UwLpEd9+7atcu+cuWKWarYwoyVZZWhlxie1+h2LsrykW2qrxIarXj7BfodpDMaSFiAoFxeXv6eBOlRtLVXPytKS0txWnyPttANM71qPh0gAjGINns10N3d7aw21F+4cMEp19XVxZYsWRLbtGmTmSaESrmG670vFFdXV/9248aNDmGFJA5B7/qW6jdh5sKFC4+Leq0w6QKabAoK+/r6fnfjxg3r6NGjVkdHh2+85Cu6q1ICYqSEiKGnA8EIwlrnz5//B7f6U43a/W716tW27OTnosGhY5oNqS4tIDXSvybciRDnzp1z80hafvjwobGB9eqb0lOCqIb5Qxuf1Ya4QlZ/WJxT+r925ePPnz8/oT53hT3CpDtxEAHU35lD1FgirBQuFBqXU9EBVkYYPRf2C58I00azQQUQLV/w9keIHOQ0kNPAp0sDXj9OJj3tDNIGf5+14zKMC7UEb9F+MCY8r98cAlkZefeJQ54yDLVsRrdv37bXrVvHRnNZXMl5JNvOsyrUPG2r31auxNn97t+/b3a6JeKSUbTjli7ICArEmU3IC6RRgvT39kv4HYRAngRgvr1QpAq2amhkbAtBBPAydn7LDq4Lb+lHpaIm4gW0RJwQSii/kYlGelB0lHfo0KHGU6dO9dFaWVMrFovtV5o3X8/O/v7+s6oeFTppXtqEAVTKSDCy6rKysne9RohFkgnBOwAFsU55+/btPGNy21+rL1oJrWWYFyqkboc4KC84YgSA2cTEBA8HxsbGTNFetmyZU1ZGweknOgSkoT0FiatgTJZRmReHmFuAOMcUBfqLzheEhG5Jwc8GEICVjtyI1dzcbF27ds06duxYUiIpXsA89BQgVKPm/SeMIlOY1MAbopWQo/UK6ycdm8wLwd9kzd1r16719snq72QCEFp/+OjRo3c6OzutM2fOZMqUwWQUKSMYqmshBY463ZafblouXbpkK3HJmYB8G0t2RsA6wAHkq8py/pWjdzrG5r3cMabV8ZD6NgtZsjMGfJhUTJsWlm6EwMdTwb59+8wasEn9GoR+nqbqjyHdJsJ7DqgQ+rwWpLeLioognAqGent731YD9ol/CweE2IIvpBOATtgD/lwvfFXYEI1Gy/Pz8wlI4v3lMaNamjkPci78cBL5nTI9GieghqkAIZjLcmG1kIWK3+7+bDrcWRkhXqgM85Re4CagtimBtgiCXYAYqbs/jBCCOx6egVzQTUB9QoG3b8qRhqKca5zTQE4DOQ3kNJDTwP+LBry76UzGDS2QcME5nSsmnafs/sSTJ09IoBMauEMEdu45372zpQAGTdzLefrrGvTvVU6grYzB8MjISNvTp0879I7TglHKnCtBsswIGDw5mQrF6xs4Puk4FNOsx88N5p6XY5KuWleqLReJHJW8AaWqZhdSnlYCisJMo4AyjXg5fXR9G9ExjqIDixdzqJK923aRLGGZisYCTLg+Z1bA7M0UUAAzSR6T01tKQAlqAHKkyAb/lPzSvcyGBcCDgQQdTBGnSa0T41oTsACUx9N9fjIWwdOgitmHbCkgsGRyjfe9jXWcPqlj9mrVLxVG5SZdSsMcVF7oL/pNitXsICjDKMoohmfGEHTW/Bhg+mAoOH36tPP9Ad9sXr161emrwb+lLy2aLl68mH/+/PloW1tbs+p+owWVj+JeCAeFw8IR4Z90acItPIuo38k8lDxhGjNYFAbTYm13DUoVvaWvO76vj+u+oQTal5TP/IEEtL2ZXPLYa9assZVmtDXbWgamYMeOHfaKFStspSKnKlVatWqVk146cuRIvP7w4cNOnXgMSAkk3czFfca7SdAZZOAwKdJX0C3ayj6QVEVSgtXY2Gjp6xJbeXJoYZ5RKcLSJ7wqzgzITotXApGtW7da2lYtKfWXjx8//pVe8nUfqS8TVyS0T/cjqAswOFbuBVrAfsjg9+zZY925c8fJ2+rqLII5a7tz6Ml80/EN9N47eDopunT6ap3ADciOsfNkbAFBFkEGD8KkWB+jvKeA5w19T1T54MGD+L3B0qVLrevXr6vJ7IAmAXncawAyhoYgU2VWW7YqwlklXnv3yAT/cfbsWUufitlYwhyBmZyMBo/MQRRAO3yb7eip8KHwI/nfL2QNP5Kfjq1fv97S58qq/uRBt48OE22T+L7ZEjNmHEZztEVhTtirJytwnbBei+G7CmxeJ/zV9am1aNEiVWcfhoaGWHSxyIjK7wwMDPxTZSaEbDjhNafNUIAfhQGYG2uAoYMvX77E+T/SFteqbUvrU8RqbW0NQzdQ2wMHDlg3b96MaPZvPXv27KQ6YZFcAZjBzygoCiTEZCOsAeURjPB1Jie8DbKCdsUGXcQC3FFdvnw5vofPpEDssHv3bhMD9InPm+L3FWGTkFMXi2FQd1bTKQjjAlO9Pi7RF2Qn4UKeixuOubUKil7TTrFP2yECWg0NDdbevXsdq6iv55IpNfCHBCJFfZdrnThxwmK3AbTe/Fn5hD+q2CvsEbIgmBggtPmrb/hQlk4eQPNmbUARfLfB+sA+XaG4oV6B0df0/KJcg5utoG43rpnvUYB1U98LfKBdx/g6n2YwcMx/SGgCoIzMfyYWIN5xMNbA4DBHXIM75jIhkQtl6lhAsRjTXsVpk2BWdrZdBseV36CQi3MQn2fg7ErMOgPPaPDqN405dTMBMzCeKIPBMmiD/KYei6ENYJ5mEDyNElAAyGBN2X10Nn30OjMwzDPrnb4X9A0PbzldbwZnBugtp+ube5/TQE4DOQ3kNBBEA/8FSS7Rlqfcs5YAAAAASUVORK5CYII=) 2x, url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACAAAAAgCAYAAAEEfUpiAAAAAXNSR0IArs4c6QAAA9xJREFUWAntV8tLVFEYnzvvpzTazIijprZRpqRFhFLUooUglSFDs2vXInAxuBaX9RcEbVNBsHAlYtbGRUK4CnMhLoxQQ8lkZGZ0Xvf2+13m3O6dmYujhAT2wcc95zvf45zvdc61WEzABbpVW1PKAEJIECWHw5HERBIE4/fw8FDRU2w6HRY7VkqSJD3Sc9Q99lN3OBxWotHoR0j92SdV2Gy2h8IWvyBdIv08oaWlpQT33Kq0adjp7Ozs54GBgXxjY2OfgbG1tXVhaWlJO0Rvb++xYFA1bG1tPZ6fny8J4sHBgTbWhyOCPSRKAFmW34J5Twic/1dCvEZxsDRMe85i3kefMvB2u30ACtxAG1B/3pp6paampufIlAIVaD4tD46OjhTsqgBJn15aHyhpf3//E5JV2t7e1tNVfrfbbfF4PMwygwK9MjEO+ny+F8lkspjJZBRiKpVS4vF4HikbB5NTMPJrdi7SeW5HmYeWi2U0FBxoFx7oqEpwIw/SCNtONpv9gsXTOQ0hvM/cYfuBsL9Se+W8KmEgqyWK1+sNQIDdsIpPKKpcYPy13Jibm9sZHBzMIoW/d3R0vMcaG7cpOJubm4s4/yaPoIfJyUmlUCgofr9/GNKVRjWF0UQiUTg+PtbLGsaBQGAU3DxSTfDDgS83NjYMQvoJFDyDpKkCnr2jra1tSy8kxsvLy4zKbaDpEbCmFtBN9ITc+vq6WomsxpWVFaW9vf0n1jvJpAfN4zoiy/U6Svea1WoNkg4H/sJnFfiVU6AGtRRwkdukIrFd9nGWs9bPMf4P/4gHzIJYuT0GU4rFYmr7WVtbkzEXWMn71+d29LYrrPPFxUVlenqa91sGV1QUltgc6j3EmTeGruZ9IC5b8VTDrX0PGvkSE6l+JgOmfUGnjSes6vxo2B9wh1uKxeIrPIcyGJdyudwb3ME/wM+aEyE63Y1QNsxTOSKRSGcwGLwDdz8RHuATo7u7W4YxtU319PTIu7u7attBmOTx8XFlbGyshJ62B8+1UA/wVGGi8caurq5vExMTSjqdVoaGhvLob1XvHdEoa335zGxoaBihLmCVB0EzBTJHnE7nMJ94U1NTci0DJ9G4gfL9EYa+ekJt2BAFKHg3FAot9Pf354XLTzLMdfIiR2SXyzUIHZeBp/IA+FVgKHjBx6BoBN7IzczM1GOfIStgA+8ge6OswzQHTBcgKIBJxDhexUb68I/xFOMY/gWq3IobOY37bxXP3NdY59W1CTwEmt5C9WwA8moW06AXyNrnc4cvd8oTWWosO/7fpIEpYBYoyhHD2lDvBmpLG8vrTPVupvji0H8DAsFwgXvDpDQAAAAASUVORK5CYII=) 1x) 9 9, auto !important;
      .footer-forehead-left {
        position: relative;
        z-index: 1;
        width: 440px;
        height: auto;
        mix-blend-mode: normal;
        display: flex;
        flex-direction: column;
        justify-content: flex-start;
        align-items: flex-start;
        gap: 24px;
        order: 0;
        flex-shrink: 0;

        .top {
          position: relative;
          z-index: 1;
          width: 160px;
          height: 32px;
          border-radius: 6px;
          mix-blend-mode: normal;
          // display: flex;
          order: 0;
          flex-shrink: 0;

          .txt {
            display: flex;
            margin: 0px;
            width: 100%;
            text-align: left;
            margin-left: 30px;
            margin-top: -50px;
            color: rgba(29, 33, 41, 1);
            font-size: 21.999999999999986px;
            line-height: 22px;
            font-weight: 700;
            font-family: "Kalam-Bold";
            letter-spacing: 0px;
            white-space: nowrap;
            text-decoration-line: none;
            top: -00px;
          }
          .img {
            position: absolute;
            z-index: 1;
            border: unset !important;
            box-shadow: unset;
            left: 2px;
            top: -50px;
            width: 24px;
            height: 24px;
            mix-blend-mode: normal;

            background-image: url(https://img.jsdesign2.com/assets/element/js_t5Ay7g8MlE0/image/4342a4510936cac29b845927f237ba2b50e9744d.png);
            background-size: 24px 24px; /* 将背景图片缩放到 24px x 24px */
          }
          .txt-2 {
            display: flex;
            margin-top: 20px;
            color: rgba(29, 33, 41, 1);
            font-size: 16px;
            line-height: 24px;
            font-weight: 400;
            font-family: "HarmonyOSSansSC-Regular";
            letter-spacing: 0px;
            white-space: pre-wrap;
          }
          .e-mail {
            position: relative;
            z-index: 3;
            width: unset;
            height: auto;
            mix-blend-mode: normal;
            display: flex;
            flex-direction: column;
            justify-content: flex-start;
            align-items: flex-start;
            gap: 16px;
            order: 2;
            min-height: auto;
            align-self: stretch;

            .input-box {
              .input-txt {
                display: flex;
                position: relative;
                top: 40px;
                border: 2px solid purple;
              }
            }
            .e-mail-icon {
              position: relative;
              z-index: 2;
              width: auto;
              height: 52px;
              box-shadow: 4px 4px 0px rgba(0, 0, 0, 1);
              border-radius: 4px;
              mix-blend-mode: normal;
              display: flex;
              justify-content: center;
              align-items: center;
              padding: 0px 24px 0px 24px;
              background: rgba(0, 89, 255, 1);
              box-sizing: border-box;
              gap: 8px;
              order: 1;
              min-width: auto;
              left: 200px;
              top: -20px;
              .icon-describe {
                position: relative;
                display: flex;
                flex-direction: column;
                z-index: 0;
                justify-content: start;
                height: 32px;
                mix-blend-mode: normal;
                color: rgba(255, 255, 255, 1);
                font-size: 20px;
                line-height: 32px;
                font-weight: 400;
                opacity: 1;
                font-family: "HarmonyOSSansSC-Regular";
                letter-spacing: 0px;
                white-space: nowrap;
                order: 0;
                width: auto;
              }
            }
          }
        }
      }
      .footer-forehead-center {
        position: relative;
        z-index: 2;
        width: unset;
        height: auto;
        mix-blend-mode: normal;
        display: flex;
        justify-content: center;
        align-items: flex-start;
        order: 1;
        flex: 1;

        .ffc1 {
          position: relative;
          z-index: 1;
          width: auto;
          height: auto;
          mix-blend-mode: normal;
          display: flex;
          flex-direction: column;
          justify-content: flex-start;
          align-items: flex-start;
          overflow: hidden;
          gap: 16px;
          order: 0;
          min-width: auto;
          margin-bottom: 10px;
          .ffc1-head {
            color: rgba(29, 33, 41, 1);
            font-size: 16px;
            line-height: 24px;
            font-weight: 700;
            font-family: "HarmonyOSSansSC-Bold";
            letter-spacing: 0px;
            white-space: pre-wrap;
          }
          .ffc1-container {
            position: relative;
            z-index: 2;
            width: 180px;
            height: auto;
            mix-blend-mode: normal;
            display: flex;
            flex-direction: column;
            justify-content: flex-start;
            align-items: flex-start;
            order: 1;
            min-height: auto;
          }
          .ffc1-container > div {
            margin-bottom: 10px; /* 设置子元素之间的间距 */
          }

          .ffc1-container > div:last-child {
            margin-bottom: 0; /* 排除最后一个子元素的底部间距 */
          }
        }

        .ffc2 {
          position: relative;
          z-index: 2;
          width: auto;
          height: auto;
          mix-blend-mode: normal;
          display: flex;
          flex-direction: column;
          justify-content: flex-start;
          align-items: flex-start;
          overflow: hidden;
          gap: 16px;
          order: 1;
          min-width: auto;
          .ffc2-head {
            display: inline;
            margin: 0px;
            width: 100%;
            text-align: left;
            position: relative;
            display: flex;
            flex-direction: column;
            z-index: 0;
            justify-content: start;
            width: 180px;
            mix-blend-mode: normal;
            color: rgba(29, 33, 41, 1);
            font-size: 16px;
            line-height: 24px;
            font-weight: 700;
            opacity: 1;
            font-family: "HarmonyOSSansSC-Bold";
            letter-spacing: 0px;
            white-space: pre-wrap;
            order: 0;
            height: auto;
          }
          .ffc2-container {
            position: relative;
            z-index: 2;
            width: 180px;
            height: auto;
            mix-blend-mode: normal;
            display: flex;
            flex-direction: column;
            justify-content: flex-start;
            align-items: flex-start;
            order: 1;
            min-height: auto;
          }
          .ffc2-container > div {
            margin-bottom: 10px; /* 设置子元素之间的间距 */
          }

          .ffc2-container > div:last-child {
            margin-bottom: 0; /* 排除最后一个子元素的底部间距 */
          }
        }
      }
      .footer-forehead-right {
        position: relative;
        z-index: 3;
        width: 220px;
        height: auto;
        mix-blend-mode: normal;
        display: flex;
        flex-direction: column;
        justify-content: flex-start;
        align-items: flex-start;
        gap: 16px;
        order: 2;
        flex-shrink: 0;

        .right-txt {
          position: relative;
          display: flex;
          flex-direction: column;
          z-index: 0;
          justify-content: start;
          width: unset;
          mix-blend-mode: normal;
          color: rgba(29, 33, 41, 1);
          font-size: 16px;
          line-height: 24px;
          font-weight: 700;
          opacity: 1;
          font-family: "HarmonyOSSansSC-Bold";
          letter-spacing: 0px;
          white-space: pre-wrap;
          order: 0;
          height: auto;
          align-self: stretch;
        }
        .right-icon {
          position: relative;
          z-index: 2;
          width: unset;
          height: 24px;
          mix-blend-mode: normal;
          display: flex;
          justify-content: flex-start;
          align-items: center;
          gap: 14px;
          order: 1;
          flex-shrink: 0;
          align-self: stretch;
          .icon-1 {
            position: relative;
            z-index: 0;
            border: unset !important;
            box-shadow: unset;
            width: 22.5px;
            height: 20px;
            mix-blend-mode: normal;
            display: flex;

            background-image: url(https://img.jsdesign2.com/assets/element/js_t5Ay7g8MlE0/image/91271b44771e56711fb1b8dc573e525b07c9e330.png);
            background-size: cover; /* 让图片覆盖整个盒子 */
            background-position: center; /* 图片居中对齐 */
            background-repeat: no-repeat; /* 防止图片重复 */
            order: 3;
            flex-shrink: 0;
          }
          .icon-2 {
            position: relative;
            z-index: 1;
            border: unset !important;
            box-shadow: unset;
            width: 20px;
            height: 20px;
            mix-blend-mode: normal;
            display: flex;
            background-size: cover; /* 让图片覆盖整个盒子 */
            background-position: center; /* 图片居中对齐 */
            background-repeat: no-repeat; /* 防止图片重复 */
            background-image: url(https://img.jsdesign2.com/assets/element/js_t5Ay7g8MlE0/image/bc8e20bb3a32f0ba328674b6f16f1946ebb77106.png);
            order: 4;
            flex-shrink: 0;
          }
        }
      }
    }
    .footer-bottom {
      position: relative;
      z-index: 2;
      width: unset;
      height: auto;
      mix-blend-mode: normal;
      display: flex;
      flex-direction: column;
      justify-content: flex-start;
      align-items: flex-start;
      gap: 32px;
      order: 1;
      min-height: auto;
      align-self: stretch;
      .footer-bottom-container-head {
        position: relative;
        width: 1200px;
        max-width: 1200px;
        /* 设置最小宽度 */
        margin: 0 auto;
        z-index: 0;

        height: 1px;
        mix-blend-mode: normal;
        display: flex;
        background: rgba(201, 205, 212, 1);
        order: 0;
        flex-shrink: 0;
        align-self: stretch;
      }
      .footer-bottom-container {
        position: relative;
        z-index: 2;
        width: unset;
        height: auto;
        mix-blend-mode: normal;
        display: flex;
        justify-content: space-between;
        align-items: flex-start;
        order: 1;
        min-height: auto;
        align-self: stretch;
        .footer-left {
          position: relative;
          display: flex;
          flex-direction: column;
          z-index: 0;
          justify-content: start;
          height: 20px;
          mix-blend-mode: normal;
          color: rgba(29, 33, 41, 1);
        }
        .footer-right {
          position: relative;
          z-index: 2;
          width: 345px;
          height: auto;
          mix-blend-mode: normal;
          display: flex;
          justify-content: flex-end;
          align-items: flex-start;
          gap: 24px;
          order: 1;
          flex-shrink: 0;
        }
      }
    }
  }
}
/* footer样式结束 */
</style>
  