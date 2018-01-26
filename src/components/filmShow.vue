<template>
  <div class="filmshow-container">
      <div class="local-film-header">
            <p>{{msg}}</p>
            <a href="#">查看更多>></a>
            <div class="header-box"></div>
          </div>
        <div class="local-film-body">
            <ul>
              <li :class="[ isthird ? 'is-third' : 'is-second' ]" v-for="(item,i) in filmList" :key="i">
                <img :src="item.img" alt="">
                <p>{{item.title}}</p>
                <span>{{item.pTitle}}</span>
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
    }
},
components: {
    
},
props: ['msg', 'filmList', 'isthird']
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
    margin: 50px auto;
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
            right: 100px;
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
        ul{
            li{
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
            .is-third{
                    width: 32%;
                }
            .is-second{
                width: 49%;
            }
        }
    }
}
</style>
