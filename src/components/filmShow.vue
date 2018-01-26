<template>
  <div class="filmshow-container">
      <div class="local-film-header">
            <p>{{msg}}</p>
            <a href="#">查看更多>></a>
            <div class="header-box"></div>
          </div>
          <div class="local-film-body">
            <ul>
              <li v-for="(item,i) in filmList" :key="i">
                <img :src="item.img" alt="">
                <p>{{item.title}}</p>
              </li>
            </ul>
          </div>
  </div>
</template>

<script>
export default {
name: 'filmshow',
data() {
    return {
        // msg: 'bendipai'
    }
},
components: {
    
},
props: ['msg', 'filmList']
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
  -webkit-padding-start: 0;
}
.filmshow-container{
    width: 100%;
    height: 100%;
    position: relative;
    margin: 0 auto;
    // background-color: pink;
    .local-film-header{
        position: relative;
        margin: 0 80px;
        border-bottom: 1px solid #eee;
        p{
            text-align: center;
            font-size: 25px;
            font-weight: bold;
            color: $color;
            letter-spacing: 3px;
            padding-bottom: 25px;
        }
        a{
            font-size: 12px;
            position: absolute;
            top: 15px;
            right: 0;
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
    .local-film-body{
        box-sizing: border-box;
        padding: 40px 80px;
        // display: flex;
        // justify-content: space-around;
        ul{
            li{
                width: 32%;
                display: inline-block;
                margin-top: 30px;
                padding: 5px;
                img{
                    display: block;
                    width: 100%;
                    height: 100%;
                }
                p{
                padding-top: 24px;
                color: #646464;
                font-size: 16px;
                font-weight: bold;
                }
                span{
                color: #aeaeae;
                font-size: 12px;
                }
            }
        }
    }
}
</style>
