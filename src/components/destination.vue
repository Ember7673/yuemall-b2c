<template>
  <div class="destination-container">
      <div class="destination w">
          <div class="des-header">
            <p>全球100+旅拍目的地</p>
            <p>GLOBAL TRAVEL DESTINATIONS</p>
            <div class="header-box"></div>
          </div>
          <div class="des-body">
            <ul>
              <li v-for="(item,i) in destination" :key="i">
                <span>{{item.title}}：</span>
                <ul class="des-list">
                  <li>
                    <a href="#" v-for="(i,index) in item.city" :key="index">{{i}}</a>
                  </li>
                </ul>
              </li>
            </ul>
          </div>
          <div class="des-footer">
            <ul>
              <li v-for="(item,i) in desList" :key="i">
                <a href="#">
                  <p>{{item.title}}</p>
                  <p>{{item.pTitle}}</p>
                  <div class="des-box"></div>
                </a>
              </li>
            </ul>
          </div>
        </div>
  </div>
</template>

<script>
export default {
data() {
  return {
    destination: [
        {
          title: '热门',
          city: ['三亚','厦门','丽江','大理','巴厘岛','罗马','皇后镇','悉尼']
        },
        {
          title: '国内',
          city: ['北京','三亚','北京','三亚','北京','三亚','北京','三亚','高雄','垦丁']
        },
        {
          title: '欧洲',
          city: ['巴黎','普罗旺斯','罗马','巴黎','普罗旺斯','罗马','巴黎','普罗旺斯','罗马','巴黎','普罗旺斯','苏黎世']
        },
         {
          title: '亚洲',
          city: ['普吉岛','苏海岛','巴厘岛','普吉岛','苏海岛','巴厘岛','普吉岛','苏海岛','巴厘岛','普吉岛','苏海岛','巴厘岛']
        },
        {
          title: '大洋洲',
          city: ['奥克兰','皇后镇','基督城','墨尔本','悉尼']
        },
        {
          title: '美洲',
          city: ['塞班','洛杉矶']
        }
    ],
    desList:[
      {
        title: '特别推荐',
        pTitle: 'GLOBAL TRAWEL DESTINATIONS'
      },
      {
        title: '本地拍',
        pTitle: 'GLOBAL TRAWEL DESTINATIONS'
      },
      {
        title: '全国拍',
        pTitle: 'GLOBAL TRAWEL DESTINATIONS'
      },
      {
        title: '亚洲拍',
        pTitle: 'GLOBAL TRAWEL DESTINATIONS'
      },
      {
        title: '全球拍',
        pTitle: 'GLOBAL TRAWEL DESTINATIONS'
      },
      {
        title: '客片展示',
        pTitle: 'GLOBAL TRAWEL DESTINATIONS'
      }
    ]

  }
}
}
</script>

<style lang="scss" scoped>
$color: #19A9E8;
.destination-container{
    position: relative;
    margin-bottom: 130px;
    .destination{
        box-sizing: border-box;
        .des-header{
            padding-top: 112px;
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
        .des-body{
          margin-top: 45px;
          ul{
            list-style: none;
            -webkit-padding-start: 0;
            li{
              display: flex;
              // justify-content: flex-start;
              margin-top: 20px;
              flex-wrap: wrap;
                  margin-left: 200px;
              span{
                  color: $color;
              }
              .des-list{
                display: inline;
                li{
                  margin: 0;
                  a{
                      border: 1px solid #888;
                      color: #888;
                      padding: 3px 6px;
                      border-radius: 4px;
                      margin-left: 5px;
                      margin-bottom: 5px;
                      font-size: 12px;
                  }
                }
              }
            }
          }
        }
        .des-footer{
          margin-top: 60px;
          ul{
              width: 1000px;
              margin: 0 auto;
              display: flex;
              justify-content: space-around;
              li{
              width: 150px;
              height: 205px;
              display: inline-block;
              background-color: rgba(0, 0, 0, .5);
              a{
                  display: block;
                  padding-top: 70px;
                  p{
                  text-align: center;
                  font-size: 20px;
                  font-weight: bold;
                  color: #fff;
                  letter-spacing: 3px;
                  
                  }
                  p:nth-child(2){
                  font-size: 12px;
                  font-weight: normal;
                  letter-spacing: 1px;
                  }
                  .des-box{
                  width: 70px;
                  height: 5px;
                  background-color: #fff;
                  margin: 10px auto;
                  }
              }
            }
          }
        }
    }
}
</style>
