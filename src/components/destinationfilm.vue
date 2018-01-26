<template>
    <div>
        <div class="des-footer">
            <ul>
              <li v-for="(item,i) in desList" :key="i" :style="item.bg">
                <a href="#">
                  <img :src="item.src" alt="">
                  <p>{{item.title}}</p>
                  <p>{{item.pTitle}}</p>
                  <div class="des-box"></div>
                </a>
              </li>
            </ul>
        </div>
    </div>
</template>

<script>
export default {
data() {
    return{
        desList:[
      {
        src: '/static/image/icon-1.png',
        bg: {
            backgroundImage: "url(/static/image/bg-1.png)",
            backgroundRepeat: "no-repeat",
            backgroundSize: "cover"
          },
        title: '特别推荐',
        pTitle: 'GLOBAL TRAWEL DESTINATIONS'
      },
      {
        src: '/static/image/icon-2.png',
        bg: {
            backgroundImage: "url(/static/image/bg-2.png)",
            backgroundRepeat: "no-repeat",
            backgroundSize: "cover"
          },
        title: '本地拍',
        pTitle: 'GLOBAL TRAWEL DESTINATIONS'
      },
      {
        src: '/static/image/icon-3.png',
         bg: {
            backgroundImage: "url(/static/image/bg-3.png)",
            backgroundRepeat: "no-repeat",
            backgroundSize: "cover"
          },
        title: '全国拍',
        pTitle: 'GLOBAL TRAWEL DESTINATIONS'
      },
      {
        src: '/static/image/icon-4.png',
         bg: {
            backgroundImage: "url(/static/image/bg-4.png)",
            backgroundRepeat: "no-repeat",
            backgroundSize: "cover"
          },
        title: '亚洲拍',
        pTitle: 'GLOBAL TRAWEL DESTINATIONS'
      },
      {
        src: '/static/image/icon-5.png',
         bg: {
            backgroundImage: "url(/static/image/bg-5.png)",
            backgroundRepeat: "no-repeat",
            backgroundSize: "cover"
          },
        title: '全球拍',
        pTitle: 'GLOBAL TRAWEL DESTINATIONS'
      },
      {
        src: '/static/image/icon-6.png',
         bg: {
            backgroundImage: "url(/static/image/bg-6.png)",
            backgroundRepeat: "no-repeat",
            backgroundSize: "cover"
          },
        title: '客片展示',
        pTitle: 'GLOBAL TRAWEL DESTINATIONS'
      }
    ]
    }
}
}
</script>

<style lang="scss" scoped>
.des-footer{
          margin-top: 60px;
          ul{
              width: 1000px;
              margin: 0 auto;
              display: flex;
              justify-content: space-around;
              li{
                position: relative;
                width: 150px;
                height: 205px;
                display: inline-block;
                background-color: rgba(0, 0, 0, .5);
              a{
                  display: block;
                  padding-top: 40px;
                  img{
                    width: 30px;
                    height: auto;
                    display: block;
                    position: relative;
                    margin: 0 auto;                    
                  }
                  p{
                    text-align: center;
                    font-weight: bold;
                    color: #fff;
                    margin: 0;
                    position: absolute;
                  }
                  p:nth-child(2){
                    // margin: 20px 0 0 0;
                    font-size: 14px;
                    letter-spacing: 3px;
                    bottom: 60px;
                    left: 50%;
                    transform: translateX(-50%);
                  }
                  p:nth-child(3){
                    font-size: 12px;
                    font-weight: normal;
                    letter-spacing: 1px;
                    bottom: 20px;
                  }
                  .des-box{
                    position: absolute;
                    bottom: 10px;
                    left: 50%;
                    width: 70px;
                    height: 3px;
                    background-color: #fff;
                    transform: translateX(-50%);
                  }
              }
            }
          }
        }

</style>
