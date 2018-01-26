<template>
  <div>
      <div class="des-header w" style="background: url(/static/image/Localfilm.png) no-repeat center">
            <p>{{headerTitle}}</p>
            <p>{{headerPtitle}}</p>
            <a :class="[ ishave ? 'is-have' : 'no' ]" href="#">查看更多>></a>
            <div class="header-box"></div>
          </div>
  </div>
</template>

<script>
export default {
data() {
  return{

  }
},
props: ['ishave', 'headerTitle', 'headerPtitle']
}
</script>

<style lang="scss" scoped>
$color: #19A9E8;
.des-header{
    position: relative;
    border-bottom: 1px solid #eee;
    margin-top: 70px;
    padding: 30px;
    p{
      text-align: center;
      font-size: 35px;
      font-weight: bold;
      color: $color;
      letter-spacing: 3px;
      margin: 0;
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
      bottom: 0;
      transform: translateX(-50%);
    }
    .is-have{
      position: absolute;
      top: 15px;
      right: 20px;
      border: 1px solid #000;
      padding: 5px 10px;
    }
    .no{
      display: none;
    }
}

</style>
