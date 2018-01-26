<template>
  <div>
    <!-- 头部 -->
      <header>
        <!-- 轮播图 -->
        <!-- <div class="swiper">
          <div class="block">
            <el-carousel height="880px">
              <el-carousel-item>
                <img src="http://fileserver.yueshijue.com/fileService/uploads/2017/12/28/15144285476756.jpg" alt=""> 
              </el-carousel-item>
              <el-carousel-item>
                <img src="http://fileserver.yueshijue.com/fileService/uploads/2017/12/28/15144282241981.jpg" alt=""> 
              </el-carousel-item>
              <el-carousel-item>
                <img src="http://fileserver.yueshijue.com/fileService/uploads/2017/12/28/15144284369625.jpg" alt=""> 
              </el-carousel-item>
            </el-carousel>
          </div>
        </div> -->
        <!-- 导航栏 -->
        <div class="navbar w">
          <!-- <div class="logo">
            <span>YOU</span><span>LOGO</span>
            </div>
            <div class="navbarList">
              <ul>
                <li>
                    <a href="#" class="active"><span>首页</span></a>
                </li>
                <li>
                    <a href="#"><span>特别推荐</span></a>
                </li>
                <li>
                    <a href="#"><span>本地拍</span></a>
                </li>
                <li>
                    <a href="#"><span>全国拍</span></a>
                </li>
                <li>
                    <a href="#"><span>亚洲拍</span></a>
                </li>
                <li>
                    <a href="#"><span>全球拍</span></a>
                </li>
                <li>
                    <a href="#"><span>客片展示</span></a>
                </li>
                <li>
                  <a href="#">
                    <span>
                      <a href="#">
                        登录
                      </a>
                      <a href="#">
                        注册
                      </a>
                    </span>
                  </a>
                  
                </li>
              </ul>
          </div> -->
          <!-- 搜索框 -->
          <!-- <div class="search">
            <p>
              目的地：三亚 海南 深圳 云南 澳洲 美国 法国 迪拜
            </p>
            <input type="text" name="" id="" placeholder="搜索你想要的目的地/行程......">
            <button>搜索</button>
          </div> -->
        </div>
        
      </header>

      <!-- 旅拍目的地 -->
      <nav>
        <desheader :header-title="desHeader.headerTitle" :header-ptitle="desHeader.headerPtitle"></desheader>
        <destinationlist></destinationlist>
        <destinationfilm></destinationfilm>
      </nav>
      

      <main>

        <!-- 广告 -->
        <!-- <div class="main-ad">
          <div class="ad-body">
            <div class="ad-body-left">
              <ul>
                <li><div class="ad1-1"></div></li>
                <li><div class="ad1-2"></div></li>
                <li><div class="ad1-3"></div></li>
                <li><div class="ad1-4"></div></li>
                <li><div class="ad1-5"></div></li>
              </ul>
            </div>
            <div class="ad-body-right">
              <div class="ad1-6"></div>              
            </div>
          </div>
        </div> -->

        <!-- 本地拍 -->
        <navheader :ishave="true" :header-title="film.msg"></navheader>
        <filmlist :isthird="true" :film-list="film.filmList"></filmlist>

        <!-- 亚洲拍 -->
        <navheader :ishave="true" :header-title="film.msg"></navheader>
        <filmlist :isthird="true" :film-list="film.filmList"></filmlist>


        <!-- 广告2 -->
        <div class="main-ad2">
          <div class="ad2-img">
            <img src="../assets/img/ad.jpg" alt="">
          </div>
        </div>

        <!-- 客片展示 -->
        <navheader :ishave="true" :header-title="custom.msg"></navheader>
        <filmlist :isthird="false" :film-list="custom.customList"></filmlist>

        <!-- 12项高端定制旅游 -->
        <div class="main-customization-travel w">
          <div class="travel-header">
            <p>12项高端定制旅游</p>
            <p>GLOBAL TRAWEL DESTINATIONS</p>
            <div class="header-box"></div>
          </div>
          <div class="travel-body">
            <ul>
              <li>
                <img src="../assets/img/icon.jpg" alt="">
                <p>售前售后</p>
                <p>24小时管家式服务</p>
              </li>
              <li>
                <img src="../assets/img/icon.jpg" alt="">
                <p>售前售后</p>
                <p>24小时管家式服务</p>
              </li>
              <li>
                <img src="../assets/img/icon.jpg" alt="">
                <p>售前售后</p>
                <p>24小时管家式服务</p>
              </li>
              <li>
                <img src="../assets/img/icon.jpg" alt="">
                <p>售前售后</p>
                <p>24小时管家式服务</p>
              </li>
              <li>
                <img src="../assets/img/icon.jpg" alt="">
                <p>售前售后</p>
                <p>24小时管家式服务</p>
              </li>
              <li>
                <img src="../assets/img/icon.jpg" alt="">
                <p>售前售后</p>
                <p>24小时管家式服务</p>
              </li>
              <li>
                <img src="../assets/img/icon.jpg" alt="">
                <p>售前售后</p>
                <p>24小时管家式服务</p>
              </li>
              <li>
                <img src="../assets/img/icon.jpg" alt="">
                <p>售前售后</p>
                <p>24小时管家式服务</p>
              </li>
              <li>
                <img src="../assets/img/icon.jpg" alt="">
                <p>售前售后</p>
                <p>24小时管家式服务</p>
              </li>
              <li>
                <img src="../assets/img/icon.jpg" alt="">
                <p>售前售后</p>
                <p>24小时管家式服务</p>
              </li>
              <li>
                <img src="../assets/img/icon.jpg" alt="">
                <p>售前售后</p>
                <p>24小时管家式服务</p>
              </li>
              <li>
                <img src="../assets/img/icon.jpg" alt="">
                <p>售前售后</p>
                <p>24小时管家式服务</p>
              </li>
            </ul>
          </div>
        </div>

      </main>

    <!-- 底部 -->
    <footer>
      <div class="footer">
        <p>旅游攻略 | 旅游攻略</p>
      </div>
    </footer>

  </div>
</template>

<script>
import destination from '../components/destination.vue'
import filmshow from '../components/filmShow.vue'
// import customshow from '../components/customShow.vue'
import desheader from '../components/desHeader.vue'
import navheader from '../components/navheader.vue'
import destinationlist from '../components/destinationList.vue'
import destinationfilm from '../components/destinationfilm.vue'
import filmlist from '../components/filmList.vue'

export default {
  name: "index",
  data() {
    return {
      film:{
          msg: '本地拍',
          filmList: [
            {
              img: '/static/img/local-film.jpg',
              title: '泰国普吉岛6天4晚私人订制行程（纯旅游）'
            },
            {
              img: '/static/img/local-film.jpg',
              title: '泰国普吉岛6天4晚私人订制行程（纯旅游）'
            },
            {
              img: '/static/img/local-film.jpg',
              title: '泰国普吉岛6天4晚私人订制行程（纯旅游）'
            },
            {
              img: '/static/img/local-film.jpg',
              title: '泰国普吉岛6天4晚私人订制行程（纯旅游）'
            },
            {
              img: '/static/img/local-film.jpg',
              title: '泰国普吉岛6天4晚私人订制行程（纯旅游）'
            },
            {
              img: '/static/img/local-film.jpg',
              title: '泰国普吉岛6天4晚私人订制行程（纯旅游）'
            }
          
      ],
    },
    custom:{
            msg: '客片展示',
            customList: [
              {
                img: '/static/img/kepianshow.jpg',
                title: '泰国普吉岛6天4晚私人订制行程（纯旅游）',
                pTitle: '三亚SANYA'
              },
              {
                img: '/static/img/kepianshow.jpg',
                title: '泰国普吉岛6天4晚私人订制行程（纯旅游）',
                pTitle: '三亚SANYA'
              },
              {
                img: '/static/img/kepianshow.jpg',
                title: '泰国普吉岛6天4晚私人订制行程（纯旅游）',
                pTitle: '三亚SANYA'
              },
              {
                img: '/static/img/kepianshow.jpg',
                title: '泰国普吉岛6天4晚私人订制行程（纯旅游）',
                pTitle: '三亚SANYA'
              },
              {
                img: '/static/img/kepianshow.jpg',
                title: '泰国普吉岛6天4晚私人订制行程（纯旅游）',
                pTitle: '三亚SANYA'
              },
              {
                img: '/static/img/kepianshow.jpg',
                title: '泰国普吉岛6天4晚私人订制行程（纯旅游）',
                pTitle: '三亚SANYA'
              }
            ]
      },
      desHeader: {
        headerTitle: '全球100+旅拍目的地',
        headerPtitle: 'GLOBAL TRAWEL DESTINATIONS'
      }
  }
  },
  components: {
    destination,
    filmshow,
    // customshow,
    navheader,
    destinationlist,
    destinationfilm,
    filmlist,
    desheader
  }
}

</script>

<style lang="scss" scoped>
  $color: #19A9E8;
a{
  text-decoration: none;
  color: #000;
}
ul{
  list-style: none;
}
.w{
   width: 1260px;
   margin: 0 auto;
}
.active{
  color: $color;
}
// 头部开始
header {
  position: relative;
  .swiper{
    position: absolute;
    // margin: 0 auto;
    top: 0;
    left: 50%;
    transform: translateX(-50%);
    width: 100%;
    // height: 880px;
    z-index: 1;
  }
  .navbar{
    position: relative;
    height: 880px;
    background-color: pink;
    .logo{
      position: absolute;
      top: 58px;
      left: 25px;
      z-index: 9999;
      span{
        font-size: 30px;
        font-weight: 800;
      }
      span:first-child{
        color: $color;
      }
      span:last-child{
        color: #fff;
      }
    }
    .navbarList{
      width: 844px;
      height: 55px;
      background-color: #fff;
      position: absolute;
      top: 52px;
      left: 280px;
      z-index: 9999;
      ul{
        list-style: none;
        li{
          float: left;
            a{
              font-weight: bold;
              padding: 17px 0 17px 26px;
              span{
                line-height: 52px;
                border-right: 1px solid #ddd;
                padding-right: 26px;
                }
            }
            a:hover{
                color: $color;
                border-bottom: 2px solid $color;
              }
        }
        li:last-child{
          span{
            border-right: 0;
            padding: 17px 26px;
          }
          a{
            padding: 0 0 17px 0;
            a:last-child{
              padding: 0;
              background-color: $color;
            }
            a:last-child:hover{
                color: #fff;
              }
          }
        }
      }
    }
    .search{
      position: absolute;
      top: 670px;
      left: 210px;
      width: 800px;
      height: 160px;
      background-color: rgba(255, 255, 255, .6);
      z-index: 9999;
      border-radius: 14px;
      padding: 36px 46px;
      box-sizing: border-box;
      input{
        width: 625px;
        height: 40px;
        border: none;
        background-color: #fff;
        padding-left: 10px;
        outline: none;
      }
      button{
        position: absolute;
        width: 80px;
        height: 40px;
        border: none;
        background-color: #00A0EA;
        color: #fff;
      }
    }
  }
 
}
// nav开始
nav{
  
}

// 广告开始
.main-ad{
  width: 100%;
  height: 688px;
  position: relative;
  margin: 0 auto;
  box-sizing: border-box;
  background-color: pink;
  .ad-body{
    .ad-body-left{
      width: 1570px;
      ul{
        li{
          float: left;
        }
      }
      .ad1-1{
        width: 860px;
        height: 365px;
        background-color: red;
      }
      .ad1-2{
        width: 708px;
        height: 365px;
        background-color: yellow;
      }
      .ad1-3{
         width: 355px;
        height: 320px;
        background-color: yellowgreen;
      }
      .ad1-4{
         width: 502px;
        height: 320px;
        background-color: black;
      }
      .ad1-5{
         width: 708px;
        height: 320px;
        background-color: blue;
      }
    }
    .ad-body-right{
      position: absolute;
      top: 0;
      right: 0;
      .ad1-6{
        width: 353px;
        height: 688px;
        background-color: green;
      }
    }
  }
}

// 本地拍开始
.mian-loacl-film{
  
}

// 地图
.main-map{
  position: relative;
  width: 1920px;
  margin: 0 auto;
}

// 广告2
.main-ad2{
  position: relative;
  margin: 0 auto;
  width: 100%;
  height: 100%;
  .ad2-img{
    img{
      width: 100%;
      height: 100%;
    }
  }
}

// 12项高端定制
.main-customization-travel{
  margin-top: 125px;
  border-bottom: 1px solid #eee;
    .travel-header{
      border-bottom: 1px solid #eee; 
      p{
          text-align: center;
          font-size: 35px;
          font-weight: bold;
          color: $color;
          letter-spacing: 3px;
        }
        p:nth-child(2){
          font-size: 12px;
          font-weight: normal;
          letter-spacing: 1px;
        }
        .header-box{
          width: 70px;
          height: 5px;
          background-color: $color;
          position: absolute;
          left: 50%;
          transform: translateX(-50%);
        }
    }
    .travel-body{
      position: relative;
      margin-top: 70px;
      padding: 0 150px;
      // display: flex;
      // justify-content: space-around;
      ul{
        li{
          width: 15%;
          display: inline-block;
          // width: 100%;
          // height: 100%;
          border: 2px solid #666;
          margin-top: 10px;
          padding: 10px 0;
          img{
            display: block;
            width: 100px;
            position: relative;
            margin: 0 auto;
          }
          p{
            font-size: 12px;
            text-align: center;
            color: #666;
            font-weight: bold;
          }
        }
      }
    }
}


// 底部
.footer{
  height: 166px;
  width: 100%;
  position: relative;
  margin: 0 auto;
  background-color: #1C1C1C;
  margin-top: 50px;
  p{
    color: #ffffff;
    text-align: center;
    padding-top: 50px;
  }
}
</style>
