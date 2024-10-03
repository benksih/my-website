<script setup>
import { reactive, toRefs } from 'vue'

const state = reactive({
  circleUrl:
    'https://cube.elemecdn.com/3/7c/3ea6beec64369c2642b92c6726f1epng.png',
  squareUrl:
    'https://cube.elemecdn.com/9/c2/f0ee8a3c7c9638a54940382568c9dpng.png',

})

const { circleUrl, squareUrl, sizeList } = toRefs(state)
import { ref } from 'vue'


const isCollapse = ref(true)
const tableData = [
  {
    name: "示例文件1",
    time: "2024-09-21",
    size: "50kb",
  },
  {
    name: "示例文件1",
    time: "2024-09-21",
    size: "50kb",
  },
  {
    name: "示例文件1",
    time: "2024-09-21",
    size: "50kb",
  },
  {
    name: "示例文件1",
    time: "2024-09-21",
    size: "50kb",
  },
  {
    name: "示例文件1",
    time: "2024-09-21",
    size: "50kb",
  },
  {
    name: "示例文件1",
    time: "2024-09-21",
    size: "50kb",
  }, {
    name: "示例文件1",
    time: "2024-09-21",
    size: "50kb",
  }, {
    name: "示例文件1",
    time: "2024-09-21",
    size: "50kb",
  }
]
</script>
<template>
  <div class="common-layout">
    <el-container>
      <el-header>

        <el-avatar :size="28" :src="circleUrl" style="margin-top: 15px;"></el-avatar>
        <el-button round style="margin-bottom:20px;margin-left:15px;height: 28px;color: #495366;"
          color="#F1F3F8" type="primary" like="ture" href="https://pan.baidu.com/disk/cert/team/create" target="_blank" rel="noopener noreferrer">创建企业/团队
        </el-button>
        <el-button round style="margin-bottom:20px;margin-left:15px;height: 28px;color: #64360D;"
          color="#ebb563">会员中心</el-button>
        <el-button round style="margin-bottom:20px;margin-left:15px;height: 28px;color: #05082c;"
          color="#FEF2EF">SVIP年卡低至6.6折！
        </el-button>
        <img src="https://fenwan.cdn.bcebos.com/cms/gamenow/webgame/2024-8/1724371116286/026949776b03.png"
          style="height: 28px;width: 28px;margin-left: 15px;">
          <img src="https://tse1-mm.cn.bing.net/th/id/OIP-C.n-WFywdoGQDdChqg2Qlh0QAAAA?w=169&h=180&c=7&r=0&o=5&dpr=1.5&pid=1.7" style="height: 10px;width: 10px;margin-bottom: 19px;"
           >
        <el-button type="info" :icon="Message" circle color="#F1F3F8"
          style="margin-left: 1030px;margin-bottom:20px"><img
            src="https://s1.4sai.com/prevfiles/f9f838b6c55c4db9b29683012e8ed338.png?e=1735488000&token=1srnZGLKZ0Aqlz6dk7yF4SkiYf4eP-YrEOdM1sob:mtR4hcgQBrIgC28R3PL5qIyuDLo="
            style="height: 18px;width: 18px;">
        </el-button>
        <el-button type="info" :icon="Message" circle color="#F1F3F8" style="margin-bottom:20px"><img
            src="https://tse3-mm.cn.bing.net/th/id/OIP-C.r7Vvkea7uEF8nQdkt2UyFAHaHa?w=157&h=180&c=7&r=0&o=5&dpr=1.5&pid=1.7"
            style="height: 18px;width: 18px;">
        </el-button>
      </el-header>
      <el-container>
        <el-aside style="width: 79.33px;height: 880px;">
          <el-menu class="el-menu-vertical-demo" :collapse="isCollapse" @open="handleOpen" @close="handleClose">
            <el-menu-item index="1">
              <el-icon>
                <div class="img"><img
                    src="https://nd-static.bdstatic.com/m-static/v20-main/home/img/icon-home-new.b4083345.png" alt=""
                    style="height: 24px;width: 24px;"></div>
              </el-icon>
              <p class="text">首页</p>
            </el-menu-item>
          </el-menu>
          <el-menu class="el-menu-vertical-demo" :collapse="isCollapse" @open="handleOpen" @close="handleClose">
            <el-menu-item index="2">
              <el-icon>
                <div class="img"><img
                    src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAEgAAABICAYAAABV7bNHAAAACXBIWXMAACE4AAAhOAFFljFgAAAAAXNSR0IArs4c6QAAAARnQU1BAACxjwv8YQUAAASoSURBVHgB7ZtNbBtFFMf/s3ZjmwNxeqioEJAUkBCKRFqCBEGpQtQg6IFScaDiQiU4tCcc0hKaHDCHNMRuUveEhIRkkIrIAZoe+GqqYIgIHAr40AISH3ZBgMQBp6gibmLvMM9pqoZm1mvHs7ux5yclm92ZVbI/vfdm1pkBNBqNRqPRaDQaTeUwrJOBwXiPsYndZ5qFNjCjGdVg8os+IM0CZnoseiQLD1GVoEg0GvYv3vQCZyzCwMOoKTxlwJeMjRx6Cx6gYkGHhmKvqBGzGsb5lNFk9rsdUbYFDUZHW4tLvlPixw44BAeyBsfe+NGX0nAJn51OJKew5PtU2LwHDiJ+X1h8O9DV3Ye52enP4AK2ImhgOJYRHVvhLmleYP3jY4dTcJCygqjmiF5ReAQONs9gpsUxa9mxRiOjpaCrdSeDDU/1I6OloIHhsSQDexZ1AhV9/6biI5VElFRQJHo87F9ayqEeMXn/sdHBhJ2uhqzBV1jsQb1isOOl2mqnq7TFZD2oZ8TAI0pI2fIhF2TwO1DniPqaoIHIqo9UEOOG0lcJjxAWE2DLVDPQ4IhRan8kEpUGQ8MLInyhUETWpgUJGGN7ZG1aEMHQIUszLWiFQGBNQX54lJbwzTj4/D5xbMaZmTlMz3wBlfj8/lZxyP7/umcjqLvr/pIc4tHeLhx4bl9JmtN4VlAoFFx1fmfbbTgoJG0TRyfZUDWopaW5JKmv92E4hWcFBYMBaZuTKed6kaaHbL/3bmy9ZQvu2nY7QsEmISdY9r6VlHv3/Y/wS+Y3qMI1QZ3b29G5o730oNWyknIqRznHBZGQp596/NoIVQso5TaLSJwU0VRrHK1BNHQv147ayVmBolEFjgkiOU/s7oUqZue+hgocSTEqxCrlnBH1Z1rUIRU4EkH0yqAKlXII5RFEo5WKmpPP53H6gxmc+/YCVKJekI3iSQ/7+59/4e/cJeTm/ylde2CHXGxO9Eu+M4U/xD2qUSqIao9snvNz5ldc+P4nnP/ux2tSrmezmON0br9REMl5/c1Jcc8lOIFSQbdu3bLqnCKFRpvPxVc+fwWVQhGTPDnlmBxCqaDr37wpYibf+9j2wy0s5Fedn/vmPE5/OFOV2PWgNsVallOkmpGGii+9oy1/YKZ2pLJCqaCQeOms9uEonY4ee6NUx9aqUU6hVFDy5Kl1p4SbcgilE0Wn64UK9H81yqAFXUW2UMpi+Yt5EQ0EW+Tza12XCjINw7W1yW4Qj6+9Flu+/AWFBhLEU7IWqaDxkSMpWnKLBoCLGYmszbpIm+YJNADFoildxW8pqBhoStR9FDH+auI1+bJgy70aX6U+yT+0c9cVBvYY6hDOeWZ8ZHCvVZ+y86CJEVpPzD2xd6uWiLqTK5pm2Q/Kbe32mZs9O9W1c1ebiEfHtkKphOQYHL0Toy//UK6vLUEESRLpxkS69WADQ2llgO22uwfNtiDiy9mzqQe7+8QMm3cwxjbaMmHOuHmi8G/+mYn4cNbuTVVv6n1xKLbfZ2AP53gS7sHLdWAcWW7wtwuXFxKJRLTiEXndu56Jw0OxDtPgrYbpnagSf8988fJCqhopGo1Go9FoGoL/ACcVnT64PD7nAAAAAElFTkSuQmCC"
                    alt="" style="height: 24px;width: 24px;"></div>
              </el-icon>

              <p class="text">收发</p>

            </el-menu-item>
          </el-menu>
          <el-menu class="el-menu-vertical-demo" :collapse="isCollapse" @open="handleOpen" @close="handleClose">
            <el-menu-item index="3">
              <el-icon>
                <div class="img"><img
                    src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAEgAAABICAYAAABV7bNHAAAACXBIWXMAACE4AAAhOAFFljFgAAAAAXNSR0IArs4c6QAAAARnQU1BAACxjwv8YQUAAAUISURBVHgB7ZxPbBRVGMC/t7vVbWJk1wMRTxujByOHqnjBmEgTjXgR5dAmHFqjiXpylcqmYNLBpK2lS1wPpoZIbA8k9ICIh0Ig6V6ACw30AOHAv01IKIFDF0JgobvzeN+Q1+wunTdvprPvzU7nlzRtZt7s7vebmfe+7+28AkRERERERLQrBHwimxvNxCGRgQAQM2l5fHzXPPiAZ0FZw0h1VF/qo5RuowBdBGgKAgQFUiZgzscgPrlveGAKPOJJ0M5f8j8ApUbQpNjBTmCJmPSP/GiuAC5xJShnjGZqS4l/2Ft+BG0Iikp01LaMGYMl2WOkBaGc6lK8yA7IQBvjVpKUoLDI4biRFAMJwiQHwVhqS/GjMm0dBf28e19/mOTU0TUwOJZ1auQoyCQwBGElRoayWUM4EgsFhfjq4aQSnZ39ogZCQZSQPgg7MfhcvFsAZsgQeogwRltBWFu1S6a8SlIYq91OW0HxcPc9DcQT9kW2VB60lklAAEgmX4T3390IG15dD5XKY7i1cAfmLlyEIKBd0Gsb1sP3X/cwScmG7Z90b4aJg4dhsXwfdKL1FrOTg6TT69i+XkinXgadaBOEgdvJWW4TAElaBFlyvukVylluq1mSckFcTjq1Tv4YjZKUCvIiZ/lYJql/xxfQyUY8lSgTtBo5HOzUv2NXkkpJygT1bP9MKKdSqcBI/gDMnRfnP1ySKgKRSaOciYPTLOe5B9P/HpeS1PPlVlCBb4ni22+9yX7eaNiGWfE5lhEvsMx46tBR68xjcI1tnsnB7JmDklDWx90f2L7fJpZ587atxDdB/Tu2rbj9w83vwcnZs3Bq9gz8xTLjZkmHj5xokMPBYxAnSY/YSfh/ZhZahZJbDMsGDBSDQUlcyPSRGbh0+YrtcVysCDwBIomrRVkthpIQDPj3P6esAhVvQSdkrqT61/YbpcVqfSAycjiykl5hqQTmS/h7ZP8B8APfBGGneu36Tetv3oGuhNezLdsn+Y1vgjCH4TiNQG4l8dtRRpLftOQW87Pf2PTORpZkbrU6duzgVUtq2SiGgZw+Oydsw0c3OzC3QjlIfZkhM7r5RUs76WMzRWtKw6lPwqCbcxkU0rv90+e2oSR+JV28fLUhOe1k75VMvsBSh2vgFy0fxXimK5KEuQxK4m1FM424r49V9TyfWinJ9BMlwzwGjoE1lxn1cIEn2a3jNNNofaWpCGXFan0GbQdK2j3wrVDO4iIraFl5ogplgprLDC+gHF71q0LpdAdKmjz0n6cAdchBlM8HYYATf7sLVJccRMuEmRtJ9ZNpOtA2oygjSbccROuUq0jSSjONOtD+3TzKwUIXay7MkzATXrh9F86xeWk3UyKtIhBPdyDW0xwXIHBEzweB+Gl6W0E1gBKsEcgTWrbdJzgOdu4ZX1wDzymW88O70nY7hbcYs+fLorRgQ4UxCgWZbEoHQg6bF5gU7RcL6khM4so9CCmU0hv7h3PC1YhCQQXjxzIFcy+EFQJ7nZtIMLBnvNiuqwztsK6ekdzrTu3k1otVq1+xFyxBSEA5NdPslmkrvSTTWvYdjxUJIRloY7icwm9ySzKlM+nC2GCpVjO3tPGVxAYsWnQjB/G0LPwnax0ZHWqTq4kyM2X2eX/ND7d4WXgzKCpGSB8F2sVeSHXGTR12opR5Ssix2oOHU4WC4Sld8e9fUxisj1pSs0KIOHzqagJKBRdr4yMiIiIiIsLJU16MP/iLELayAAAAAElFTkSuQmCC"
                    alt="" style="height: 24px;width: 24px;"></div>
              </el-icon>

              <p class="text">同步</p>

            </el-menu-item>
          </el-menu>
          <el-menu class="el-menu-vertical-demo" :collapse="isCollapse" @open="handleOpen" @close="handleClose">
            <el-menu-item index="4">
              <el-icon>
                <div class="img">
                  <img
                    src="data:image/png;base64,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"
                    alt="" style="height: 24px;width: 24px;">
                </div>
              </el-icon>

              <p class="text">AI看</p>

            </el-menu-item>
          </el-menu>
          <el-menu class="el-menu-vertical-demo" :collapse="isCollapse" @open="handleOpen" @close="handleClose">
            <el-menu-item index="4">
              <el-icon>
                <div sclass="img-bottom">
                  <img
                    src="data:image/png;base64,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"
                    alt="" style="height: 24px;width: 24px;">
                </div>
              </el-icon>
                <img src="https://tse1-mm.cn.bing.net/th/id/OIP-C.n-WFywdoGQDdChqg2Qlh0QAAAA?w=169&h=180&c=7&r=0&o=5&dpr=1.5&pid=1.7" style="height: 10px;width: 10px;margin-top: -15px;"
                >
                 <p style="display: block;margin-bottom: -25px;margin-left: -34px;"> 消息</p>
            </el-menu-item>
          </el-menu>
          <el-menu class="el-menu-vertical-demo1" :collapse="isCollapse" @open="handleOpen" @close="handleClose">
            <el-menu-item index="4">
              <el-icon style="margin-bottom: 20px;">
                <img src="https://staticsns.cdn.bcebos.com/amis/2022-11/1668677253692/appDownload.jpg" alt=""
                  style="height: 24px;width: 24px;"></el-icon>
              <p class="text-bottom">APP下载</p>
            </el-menu-item>
          </el-menu>
          <el-menu class="el-menu-vertical-demo" :collapse="isCollapse" @open="handleOpen" @close="handleClose">
            <el-menu-item index="4" @click="window.open('https://pan.baidu.com/disk/cert/submit')">
              <el-icon>
                <div class="img">
                  <img src="https://nd-static.bdstatic.com/m-static/v20-main/home/img/fea_aside_icon_cert.320ef0fb.png"
                    alt="" style="height: 24px;width: 24px;">
                </div>
              </el-icon>

              <p class="text-bottom">网盘认证</p>

            </el-menu-item>
          </el-menu>
          <el-menu class="el-menu-vertical-demo" :collapse="isCollapse" @open="handleOpen" @close="handleClose">
            <el-menu-item index="4">
              <el-icon>
                <div class="img">
                  <img
                    src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAEgAAABICAYAAABV7bNHAAAACXBIWXMAACE4AAAhOAFFljFgAAAAAXNSR0IArs4c6QAAAARnQU1BAACxjwv8YQUAAAsySURBVHgB7VxbbBxXGf7OzOx6fVnbaRInviSxeQAKEhgUJTQ0TagUeAAplkIJbR/ivMBjAm88oCRvXKTUeYJKVE2kUoGCUCIQCBCtIypBEYVQWhGIqA0ktuPYia97nZnD/5+57OzF1zkbErufMtkzZ87O7nz+/u/855zZEVgFRkZG2q1US78pcJR2D0OIXkjZjkcJQswIKa+7Qow6tnN1d/eOK6t623IHmZhUU8spCXH6kSNkRYhRKTBccIvn+jo7R5dstdSBicnpU66UZwNiDMNAY6oBCcuElUjAEMty+9CBrgWO4yCXK6BQLKqyBzHqSvdcT2fHxVrvq3mVY5N3X4CL01xOWBZa081IJhPYSMhmc5hfzJaIMjDU1bH9a5XtqggavzP1spRykMtMTHNTIzYyFhYyRFRGlaUQF7t3bDsZPV5GUKAcDqe21hakGpLYDMjlC5idW4DrulVKMoLCrfHJwSCsNhM5DL5WvmYF4mBsYuJ0cEwpaHx8vFeKxOskst50cxNaWpqwGbGYyWJufpFZmclnrL6+vi0znoKMxBkmxzTNTUsOg/02kbCICrQnUwWlIqWgsYmpESaonWTW2JjCZkahUMT0/dlQRcbt21MDgXo2OzkMTme4k2IVWalcv2FYaviAZGJj5TlxwAkxQ0hzwKJMuderjEfQ2Z948dpJefcHu4APdVJ5Cx4o7N8vwvxYI0SzgTiwaLTAMExxyKLxSD/JCRxicfDzt6rrmKhnPw3s7asvWe6dInLn78D+WwYNz29VWxwkStHUa3GscUmIeKzXwj/HgHOXoaT17AHguSc9hemCXHRRuHIf+R9Oh3W8nxzYEktFRpA+Ezf6WYmCP4j9jrZX3wS+8hIwfANaYL+5iMzp/6Dwo3uRdNcjrfibWeiCfoICUkxvg+nt83Z7Hvj6j4EXr2HdcO/ayJwZQ/bb43CnbO/cPLNg8Iv3p7f/sAhdsKALTAp/v0CewtuXkf1ge/F3XvuvHlz12SEzpIxfzqJw+R4PBzxipHdiQQVJHyRdVQH77YxSUlyzZmgjSPoeLyNEKPjlSqK+/wbQQhMFz+9d+dz2WxkUXpmGnLRLauHPUkRJdUKaLVSvqo4IY+M2P9CAuNBHkJI6qohR5FTu+6/ffY16uN2UEnQscU4KofxLU3BuZAHH/wx1wP8IPpcrvAp+JbLUHn2A+15eC0H6PMj3GXURvv9Ifz/wo7I6v/6bv6o+lQqnn80i843bcG7mPCaorepoDeF/llAkh3WmCF+5uXu3CB3QRlBoykY1MYgQEzVt3m5QD/3KX0rncW/mkf/WBIq/mCknJAitaNknRYTn80hTZGmaEdZq0tHwUagIqSDcKtt870/kRXscFF6dVgQpszW80BHKWshbhB9G/C8oS9+LuInkV8+HwO/XNGeu16T971Rm1LV8KFJ2HUr23pvFG9/JYm/B9cPGaySD/+iCuU4RoIzZpyUkBao+bMNNdugZW9bHpFcgJSDQnc+jMDJNU542rqYE9jYHDWTpxAEhPknqs2RJKSUyZUgSw9iu59L0mXSlAUd8psyouVyk3ukfk8jfuANJ5DB+m5cRbwr8RkQ8S5SOi4o6UXGcNqMvfg/GqGs3X+U9FE7OnXk4E/OQtlv2/nlqME5v6GISXV8h7EHkNV73Lv0TSpUahuHFXmRyO7UqoVRlfqQJoknP316fSZs18p3IvjuXR/Ff06FiauHvjiSCREkhypD8iw/MNxhJRn0pII7bUV3iqRboQl0UFCWGVWPfnIZzL7viORb4jQaqFRIkgFF/8tUSfKA6znwqBelby9NLkK9q9UX5+5Naiu9MQubs1Z3EEGFSqBSCCoUEJ0fJqEXYm0GZtHUwDbFNX2DoDbGo/xTWSI7/Po8clPIgpiDotRiBgqS/RXu4rSbNBem9x6I+IcbKeXuN5MCbrij5ChAatfTqomMvZd6+0oJwSx5th9iq72/O0KqgwH+K706tmRyG9M1ZzW7SMrCnlZJCvAzbr/Oz7MC8E19oh/WEPnMOoF1Bzi3qwhcKWA9EkM9Ehhr+ERVaXrjBrw/MmUx5fwsSn29DPaB3qEGqcf87j3UjNPpaWbLfm/lduRduEtZTaSQG6ndvl9bBqjO+CJlde2iFiHpQmPf4fVUwQPVDSyQNWEfSsJ7UH1ZRaFWQOxZzLtgPMeUtRimMokbNdUZvEoljtHKxJd5S1Wqgj6D7NLEVRz2MMIOG6qWYKck3gBmeBxntFizqqYy+B3drjjaC3MmVM+UV4U+IBXkzh5RgkSRINfuaYO5rhkgJPEjo86C59fVcUahlGyHCiXhWkNGdgEk9lGirfzjVgr4QyziIC2XErCJOiFoNmJ9Lw9j1/73TTZ+CMjH9B34m3WjA4BsQPkFbw4MNp1rQm5fHRXcS5nEKp3TtcJoho75EC4LDeRfXi6VZx16aIhmkRcJDDYYq68RDQZBMW5CHH4M4mCJyardhUk7et/FvW1Yd47prdLzXEjjTauJEkz6/0jbl2rOOKQZJf3F3bxvcZ3bC7Ukt+W3Ozdl4mta5apETxSgdP3nPpvbx/TCANgV1bzNxa2r1PiS7U3A/8xhkq1U+VVuBS2T+a71gJpTvWznVEl9J2hT0+Cp7Gw4n52gHnIEOSEr8won8yLJRgFGagj27TjUwSfz+uNBG0JFPLj/NqcJpXxuc4xROu1NlKx8hSRUEsa+sFFZLYYYGtRfm44eaNoL2fziF9BIrCRxOzpd3wvlUGyS3ia7fR+8hqiDowryLOLiUeYgIYpw8Ut4Fsb/Yxzpgf9EPJwNla/XRdXxUhBgr4HoxHkF8jvUqMIBWggY/mw5V5Oxvg/0chdOuVNVCohtRULROlhEU3z8YIzFFpDUPaiVyBo+143wyVeqdGJFFRBGskyEYmPqoEWIPA7QqiHHq6RY8vsMq95kghCKhVRZmZmTS3wcnfe1GfMb6Yw7ltBPE+EEv5UWpGr1UZdlY3qQ/nohHkCI55m0wdSGoJ0Ek9QBpC1U3UFWSUlZXcS1xEz0edsRFXQhifJQU9OteIquhPMSid5jJJZQTYKDRG4CuB6weHWOyuhHE6CEFXe4CvtSKahWtUvkvb7HW5UU/3arnBqq6EsTYRSS9sA04v9ULvWVRo2dnJby2PYE91upIYjK5fX9CT5dokLxn1HeT8ZKylXC8GfhjJ5H1GHBgqZ+lLXFNfLGvb0vgRPPyIXOYJtj+3JGg13h/d7e0Xjkjxibu8j2m/W2taTQ16rkrazWYo7/Hu0XgHZrKvkXJHI9Jn6ElrgMrfAWe0hguuPhrQapkkhXj+Y2hJS1g8K+g78/McXHYohXwaySjftvm+4ofHEE05YwnGrxtLWAyBvn3XHX8aS0TxJBCjBpSCvWQj2w2j/fhoVAIV2iuGnbOus6xxs+24B+0bnZksjk4DvuxHO3ese2Kwb8NJ3++wAfVb8Y3ORbCx1QYw/yq7L6Qs4ZYRUXbVj+u36zgZ3gE6uHH5nCdIohV5NLUL5dZRYFJbSbwNfODThjUOYbPFAoThp6u7UMuhAq12dn5TUWS93AT774m15UXos8Sqkocbo9PXqQVzhNc5sdU8LM8NjIWMzmKmgVVllJe6u7sGIwer5lZ3ZqYGjIgT3HZNA20EElNG+ypDNxjs52w7zKUcro6Tle2WzL15MflUGJ6hpr08j4TlUwm1aNkLCrX42fk9QQPpYpFmwhxkM3lmBDvAA+1yHO6dm4fqvW+ZXNzfmyOC/MszTkdCojaMCBiOL0p5BaG+vr6ZpZutkqoh6AY7gD50x54T2t4xB4TqJQySsq5RkOIK3Zu4fpyxAT4HxyDnP+on8COAAAAAElFTkSuQmCC"
                    alt="" style="height: 24px;width: 24px;">
                </div>
              </el-icon>
              <div style="display: flex; flex-direction: column; box-align:bottom; margin-top: 5px;">
                <p class="text-bottom">一刻相册</p>
              </div>
            </el-menu-item>
          </el-menu>
          <el-menu class="el-menu-vertical-demo" :collapse="isCollapse" @open="handleOpen" @close="handleClose">
            <el-menu-item index="4">
              <el-icon>
                <div class="img">
                  <img
                    src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAEgAAABICAYAAABV7bNHAAAACXBIWXMAACE4AAAhOAFFljFgAAAAAXNSR0IArs4c6QAAAARnQU1BAACxjwv8YQUAAAQGSURBVHgB7ZtNThsxFICfHaClLMoR0hOQ3iC5QTgBsKhQYAEs2ghVLU6piqCbdFEhSqXADcoJSG8QTtDhBuxCafJe7SSDVBSPPT8OE9WfxAYb3sw39njG7w2Ax+PxeDzTCoMpRhwcl1mhsAdAJSBYlKfTYdj/8n63dgYZMbWC9g9P9xBQjG9lHcL+stitBZCSqRQULeeegBAraSUZBQnRWiws9LYQqQqMisOhnIhABusA4kWaKWAp5z5mWkmRgsSnkyqbgVYKKbqwHerOVoRYu4nzVzHlhKSSxHUN8gZYdCNHQSW+cLcX5y8SylEUGeeX6nwgAVpBoFYHJ3KGEMK2mr42fVPICUksSSuIkVw6XfPktmrqkoGckESSeESbe0HyoKMaM5RzHy+uJA45xYGckFiScinIoZwQa0m5EzQBOSFWknIlaP/o29aE5IQU5btcK6pDbgSpK4lE2zBpiMofDo5Xdc15GkFlMKxqrqBCYUXXljdBj4McRbqm/AhiLNZ7WcZoY+dHENEPeCQYMW3s/Nykd2ttINaGRwCp39C15WqZJ+qvyQ2YiU41AmxEbYXkSpA6UIJeZVKSBnLqNRHVJ3dP0uLNZmcSkmzkKHL5LuZakq0chV7QhO8FD3ElKY4chV4Qsg64px3VmLWkuHIUWkHIehfglmCwtBvISlISOQqtoEZ9owkqTeMIhtiw7ZtWUlI5isibtEyXLMufc8gSeZIIsBM3N5ZUUho5CqvMqtqK4JyqiLzIGTyHBMitjGvgvAPduXbcfNg/x3L0tcRg5tIm45JWjmIqU882krKQo5ja4oVBYlNumcLDPSQ1hQkajfp6EzJgqstfFOLwpCrnb3kw9RleYXf+LM0U9niyxW4VUzn0YZq4COlo2zwcOolNcgW9i7+CMtPB8Wd3LSIw5tBjEKiHRJvnoGEaiESWRRScc/Hu9Svrh9TIB0U2/+cyYzmKInHe+nj4fSWq0yCBSNTMusIEEcX+51Pr0hvtCJLL6KpcRiOTaim5oe7ci3FDfrSE/wKHUK/3UrzdNL5K6ctfWCHyCmeAureUNMHdJxBnuNXM0E8x7r4+SE61sTEY8CVwHpxZnZ9ekMPqshB5s3YeQwu3e6fMbX1QXvCCDHhBBrwgA16QAS/IgBdkwAsy4AUZ8IIMeEEGvCADXpABL8hAlKAA3AcPxv2eqH8NrkG4summFURErstf5DFq6oM4d18SzLBt0y1iw0xumDusMmPEznTVpaK+rgQF4I5A1DesLoL+o15VcdrHHReS5Ohs4+3sTmQfxAq4kRSM/rcV5u/mh99TCTnsl1iazzSlaELqcKJz29qgUewyY2wFOCsl3gYexZZX5if8ftr0uXuPx+Px/B/8Bdwt73TntmMLAAAAAElFTkSuQmCC"
                    alt="" style="height: 24px;width: 24px;">
                </div>
              </el-icon>
              <div style="display: flex; flex-direction: column; box-align:bottom; margin-top: 5px;">
                <img src="https://tse1-mm.cn.bing.net/th/id/OIP-C.n-WFywdoGQDdChqg2Qlh0QAAAA?w=169&h=180&c=7&r=0&o=5&dpr=1.5&pid=1.7" style="height: 10px;width: 10px;margin-top: 30px;display: block;margin-left: 0px;">
                 
                <p style="display: block;margin-bottom: 15px;margin-left: -27px;">工具</p>
              </div>
            </el-menu-item>
          </el-menu>
        </el-aside>
        <el-main>
          <div class="common-layout">
            <el-container>
              <el-aside width="200px"> <el-menu default-active="2" class="el-menu-vertical-demo" @open="handleOpen"
                  @close="handleClose">
                  <el-sub-menu index="1" style="width: 177px;">
                    <template #title>
                      <el-icon>
                        <location />
                      </el-icon>
                      <span>我的文件</span>
                    </template>
                    <el-menu-item index="1-1"><svg xmlns="http://www.w3.org/2000/svg" width="16" height="16"
                        fill="currentColor" class="bi bi-images" viewBox="0 0 16 16">
                        <path d="M4.502 9a1.5 1.5 0 1 0 0-3 1.5 1.5 0 0 0 0 3z" />
                        <path
                          d="M14.002 13a2 2 0 0 1-2 2h-10a2 2 0 0 1-2-2V5A2 2 0 0 1 2 3a2 2 0 0 1 2-2h10a2 2 0 0 1 2 2v8a2 2 0 0 1-1.998 2zM14 2H4a1 1 0 0 0-1 1h9.002a2 2 0 0 1 2 2v7A1 1 0 0 0 15 11V3a1 1 0 0 0-1-1zM2.002 4a1 1 0 0 0-1 1v8l2.646-2.354a.5.5 0 0 1 .63-.062l2.66 1.773 3.71-3.71a.5.5 0 0 1 .577-.094l1.777 1.947V5a1 1 0 0 0-1-1h-10z" />
                      </svg>
                      <p style="margin-left: 20px;">图片</p>
                    </el-menu-item>
                    <el-menu-item index="1-2"><svg xmlns="http://www.w3.org/2000/svg" width="16" height="16"
                        fill="currentColor" class="bi bi-file-earmark" viewBox="0 0 16 16">
                        <path
                          d="M14 4.5V14a2 2 0 0 1-2 2H4a2 2 0 0 1-2-2V2a2 2 0 0 1 2-2h5.5L14 4.5zm-3 0A1.5 1.5 0 0 1 9.5 3V1H4a1 1 0 0 0-1 1v12a1 1 0 0 0 1 1h8a1 1 0 0 0 1-1V4.5h-2z" />
                      </svg>
                      <p style="margin-left: 20px;">文档</p>
                    </el-menu-item>
                    <el-menu-item index="1-3"><svg xmlns="http://www.w3.org/2000/svg" width="16" height="16"
                        fill="currentColor" class="bi bi-play" viewBox="0 0 16 16">
                        <path
                          d="M10.804 8 5 4.633v6.734L10.804 8zm.792-.696a.802.802 0 0 1 0 1.392l-6.363 3.692C4.713 12.69 4 12.345 4 11.692V4.308c0-.653.713-.998 1.233-.696l6.363 3.692z" />
                      </svg>
                      <p style="margin-left: 20px;">视频</p>
                    </el-menu-item>
                    <el-menu-item index="1-4">
                      <p>Bt</p>
                      <p style="margin-left: 20px;">种子</p>
                    </el-menu-item>
                    <el-menu-item index="1-5"><svg xmlns="http://www.w3.org/2000/svg" width="16" height="16"
                        fill="currentColor" class="bi bi-music-note" viewBox="0 0 16 16">
                        <path d="M9 13c0 1.105-1.12 2-2.5 2S4 14.105 4 13s1.12-2 2.5-2 2.5.895 2.5 2z" />
                        <path fill-rule="evenodd" d="M9 3v10H8V3h1z" />
                        <path d="M8 2.82a1 1 0 0 1 .804-.98l3-.6A1 1 0 0 1 13 2.22V4L8 5V2.82z" />
                      </svg>
                      <p style="margin-left: 20px;">音频</p>
                    </el-menu-item>
                    <el-menu-item index="1-6"><svg xmlns="http://www.w3.org/2000/svg" width="16" height="16"
                        fill="currentColor" class="bi bi-three-dots" viewBox="0 0 16 16">
                        <path
                          d="M3 9.5a1.5 1.5 0 1 1 0-3 1.5 1.5 0 0 1 0 3zm5 0a1.5 1.5 0 1 1 0-3 1.5 1.5 0 0 1 0 3zm5 0a1.5 1.5 0 1 1 0-3 1.5 1.5 0 0 1 0 3z" />
                      </svg>
                      <p style="margin-left: 20px;">其他</p>
                    </el-menu-item>
                  </el-sub-menu>
                  <el-sub-menu index="2">
                    <template #title>
                      <el-icon>
                        <location />
                      </el-icon>
                      <span>回收站</span>
                    </template>
                  </el-sub-menu>
                  <el-sub-menu index="3">
                    <template #title>
                      <el-icon>
                        <location />
                      </el-icon>
                      <span>快捷访问</span>
                    </template>
                  </el-sub-menu>
                </el-menu>
                <div class="drop-in">+ 拖入常用文件夹</div>
                <el-progress :percentage="0" :show-text="false" stroke-width="6px" style="margin-top: 570px;"/>
                <el-text size="small">400kb/∞</el-text> 
              </el-aside>
              <el-container>
                <el-header>
                  <el-button type="primary" round><svg xmlns="http://www.w3.org/2000/svg" width="16" height="16"
                      fill="currentColor" class="bi bi-box-arrow-up" viewBox="0 0 16 16">
                      <path fill-rule="evenodd"
                        d="M3.5 6a.5.5 0 0 0-.5.5v8a.5.5 0 0 0 .5.5h9a.5.5 0 0 0 .5-.5v-8a.5.5 0 0 0-.5-.5h-2a.5.5 0 0 1 0-1h2A1.5 1.5 0 0 1 14 6.5v8a1.5 1.5 0 0 1-1.5 1.5h-9A1.5 1.5 0 0 1 2 14.5v-8A1.5 1.5 0 0 1 3.5 5h2a.5.5 0 0 1 0 1h-2z" />
                      <path fill-rule="evenodd"
                        d="M7.646.146a.5.5 0 0 1 .708 0l3 3a.5.5 0 0 1-.708.708L8.5 1.707V10.5a.5.5 0 0 1-1 0V1.707L5.354 3.854a.5.5 0 1 1-.708-.708l3-3z" />
                    </svg> <el-text style="color: white;margin-left: 5px;" tag="b">上传</el-text></el-button>
                  <el-button-group style="margin-left: 20px;">
                    <el-button color="#F0F9FE" round type="primary" style="color: #66b1ff"><svg
                        xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor"
                        class="bi bi-folder-plus" viewBox="0 0 16 16">
                        <path
                          d="m.5 3 .04.87a1.99 1.99 0 0 0-.342 1.311l.637 7A2 2 0 0 0 2.826 14H9v-1H2.826a1 1 0 0 1-.995-.91l-.637-7A1 1 0 0 1 2.19 4h11.62a1 1 0 0 1 .996 1.09L14.54 8h1.005l.256-2.819A2 2 0 0 0 13.81 3H9.828a2 2 0 0 1-1.414-.586l-.828-.828A2 2 0 0 0 6.172 1H2.5a2 2 0 0 0-2 2zm5.672-1a1 1 0 0 1 .707.293L7.586 3H2.19c-.24 0-.47.042-.683.12L1.5 2.98a1 1 0 0 1 1-.98h3.672z" />
                        <path
                          d="M13.5 10a.5.5 0 0 1 .5.5V12h1.5a.5.5 0 1 1 0 1H14v1.5a.5.5 0 1 1-1 0V13h-1.5a.5.5 0 0 1 0-1H13v-1.5a.5.5 0 0 1 .5-.5z" />
                      </svg>
                      <p style="margin-left: 5px;">新建文件夹</p>
                    </el-button>
                    <el-button color="#F0F9FE" type="primary" style="color: #66b1ff"><svg
                        xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor"
                        class="bi bi-file-earmark-plus" viewBox="0 0 16 16">
                        <path
                          d="M8 6.5a.5.5 0 0 1 .5.5v1.5H10a.5.5 0 0 1 0 1H8.5V11a.5.5 0 0 1-1 0V9.5H6a.5.5 0 0 1 0-1h1.5V7a.5.5 0 0 1 .5-.5z" />
                        <path
                          d="M14 4.5V14a2 2 0 0 1-2 2H4a2 2 0 0 1-2-2V2a2 2 0 0 1 2-2h5.5L14 4.5zm-3 0A1.5 1.5 0 0 1 9.5 3V1H4a1 1 0 0 0-1 1v12a1 1 0 0 0 1 1h8a1 1 0 0 0 1-1V4.5h-2z" />
                      </svg>
                      <p style="margin-left: 5px;">新建在线文档</p>
                    </el-button>
                    <el-button color="#F0F9FE" round type="primary" style="color: #66b1ff;"><svg
                        xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor"
                        class="bi bi-download" viewBox="0 0 16 16">
                        <path
                          d="M.5 9.9a.5.5 0 0 1 .5.5v2.5a1 1 0 0 0 1 1h12a1 1 0 0 0 1-1v-2.5a.5.5 0 0 1 1 0v2.5a2 2 0 0 1-2 2H2a2 2 0 0 1-2-2v-2.5a.5.5 0 0 1 .5-.5z" />
                        <path
                          d="M7.646 11.854a.5.5 0 0 0 .708 0l3-3a.5.5 0 0 0-.708-.708L8.5 10.293V1.5a.5.5 0 0 0-1 0v8.793L5.354 8.146a.5.5 0 1 0-.708.708l3 3z" />
                      </svg>
                      <p style="margin-left: 5px;">云添加</p>
                    </el-button>
                  </el-button-group>
                  <el-input v-model="input" style="width: 240px;margin-left: 6px;" placeholder="搜索我的文件" />
                </el-header>
                <el-main>
                  <div>全部文件</div>
                  <el-table :data="tableData" style="width: 100%">
                    <el-table-column prop="name" label="文件名" width="180" />
                    <el-table-column prop="time" label="修改时间" width="180" />
                    <el-table-column prop="size" label="大小" />
                  </el-table>
                </el-main>
              </el-container>
            </el-container>
          </div>

        </el-main>
      </el-container>
    </el-container>
  </div>
</template>


<style scoped>
.drop-in {
  border: 2px dashed rgb(194, 194, 194);
  color: gray;
  text-align: center;
  height: 50px;
  width: 150px;
  margin-left: 25px;
  line-height: 50px;
  border-radius: 10px;
}

.el-menu-vertical-demo1 {
  margin-top: 335px;
}

.img {
  display: block;
  margin-top: -10px;
}

.text {
  display: block;
  margin-bottom: -20px;
  margin-left: -25px;
}

.text-bottom {
  display: block;
  margin-bottom: -20px;
  margin-left: -40px;
}

.img-bottom {
  display: block;
  margin-top: 20px;
}
</style>
